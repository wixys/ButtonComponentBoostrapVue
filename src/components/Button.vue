<template>
  <div>
    <template v-if="link">
      <b-link :href="link" target="_blank">
        <b-button
          :variant="variant"
          :size="size"
          class="m-3"
          :pill="pill"
          :squared="squared"
        >
          {{ labelName }}
          <b-icon :icon="icon" :class="iconClass"></b-icon>
        </b-button>
      </b-link>
    </template>
    <template v-else-if="setFunction">
      <b-button
        :variant="variant"
        :size="size"
        class="m-3"
        @click="setFunction"
        :pill="pill"
        :squared="squared"
      >
        {{ labelName }}
        <b-icon :icon="icon" :class="iconClass"></b-icon>
      </b-button>
    </template>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    labelName: {
      type: String,
      required: false,
    },
    variant: {
      type: String,
      required: false,
    },
    icon: {
      type: String,
      required: false,
    },
    iconClass: {
      type: String,
      required: false,
    },
    link: {
      type: String,
      required: false,
    },
    size: {
      type: String,
      required: false,
    },
    pill: {
      type: Boolean,
      required: false,
    },
    squared: {
      type: Boolean,
      required: false,
    },
    setFunction: {
      type: Function,
      required: false,
    },
  },
};
</script>
