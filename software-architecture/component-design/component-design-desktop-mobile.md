# A concept for a desktop/mobile responsive component

A lot of times the design of the mobile and desktop version differ a lot. Sometimes there is even the need to show two completely different components. In this case it could be useful to move the responsive logic into a separate component.

## Vue 3 responsive component
Vue 3 provides the option to have named slots and the option to pass data to the slots.


```typescript
<template>
  <slot name="mobile" :classMobile="cssClassMobile" />
  <slot name="desktop" :classDesktop="cssClassDesktop" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ResponsiveElement",
  data: () => ({
    cssClassMobile: "hide-on-desktop",
    cssClassDesktop: "show-on-desktop",
  }),
});
</script>
```

I like to have all the classes that control the visibility for different breakpoints in a separate file. This could look like this:

```css
<style>
.hide-on-desktop {
  display: inherit;
}

.show-on-desktop {
  display: none;
}

@media (min-width: 992px) {
  .hide-on-desktop {
    display: none;
  }

  .show-on-desktop {
    display: inherit;
  }
}
</style>
```   

The usage of the  `ResponsiveElement` will look like this:                                                              
```html
<ResponsiveElement>
  <template v-slot:mobile="{ classMobile }">
    <div :class="classMobile">Only on mobile</div>
  </template>
  <template v-slot:desktop="{ classDesktop }">
    <div :class="classDesktop">Only on desktop</div>
  </template>
</ResponsiveElement>
```

There are the two named slot that each contain another HTML element - this could also be another custom element. The classes for hiding/showing the element are added to the element via class binding.

## What are the benefits of this approach?
Should it happen that class names or breakpoints need an adjustment, having the responsive behavior encapsulated will be a big advantage as there are fewer places to do the adjustments.

Also the code appears a bit more structured since the classes for the responsiveness are clustered (put together).

In a complex application the component for the responsive behavior can be  reused really good.

## And are there any drawbacks?
Having an additional components always means that there is a need to load more JavaScript and therefore could potentially increase your loading times. But that really depends on the loading behavior - meaning for a server side rendered application this is not as relevant as for a client side rendered application.

Then there is also the question about the maintainability for future developers. When they're not used to it, they will probably use the css classes and all the benefits of the component were obsolete.

## Summary

Choose an extra component for encapsulating responsiveness strongly depends on the project. Sometimes it's enough to just use the css classes, but in other cases the encapsulation can be an advantage.
