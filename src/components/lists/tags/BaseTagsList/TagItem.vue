<template>
  <BaseLabelLinkContainer
    :link="tagMainLink"
  >
    <span class="link">
      {{ tagName }}
    </span>
  </BaseLabelLinkContainer>
</template>

<script>
import BaseLabelLinkContainer
  from '@/containers/links/BaseLabelLinkContainer.vue'
import { main as formatTagMainLink } from '#/formatters/links/tag'

export default {
  name: 'TagItem',
  components: {
    BaseLabelLinkContainer
  },
  props: {
    tagName: {
      type: String,
      required: true
    }
  },
  computed: {
    tagMainLink () {
      return formatTagMainLink({
        tagName: this.tagName
      })
    }
  }
}
</script>

<style lang="sass" scoped></style>
