<template>
    <div :style="{width: width, height: height}">
        <div class="_brandshape-border">
            <svg class="_brandshape-border--mask"
                 viewBox="0 0 124 124"
                 xmlns="http://www.w3.org/2000/svg"
                 xmlns:xlink="http://www.w3.org/1999/xlink">
                <defs>
                    <path d="M926.657 2063.072a54.39 54.39 0 0 0-2.364-4.478c-9.229-15.372-26.15-25.898-45.263-28.156-17.68-2.093-34.42 3.374-45.9 14.975a47.193 47.193 0 0 0-2.81 3.027 57.496 57.496 0 0 0-6.392 8.509c-9.435 17.744-12.366 37.944-7.84 54.036.02.072.044.142.072.212a59.865 59.865 0 0 0 2.41 5.14c8.123 15.385 22.666 27.122 38.907 31.403.764.232 7.748 2.26 17.508 2.26 6.073 0 13.224-.788 20.618-3.28 0 0 8.793-2.338 14.226-6.654 5.433-4.317 6.836-5.18 9.815-7.942 1.082-1.004 2.103-2.418 4.053-4.751 2.082-2.846 3.343-5.486 4.608-7.092l.12-.154c2.086-3.37 5.356-10.597 5.547-16.495a1.899 1.899 0 0 0-.06-.51 1.93 1.93 0 0 0 .073-.442c.294-8.615-3.654-31.763-7.328-39.608"
                          id="a"/>
                </defs>
                <use stroke="currentColor" stroke-width="4" xlink:href="#a" transform="translate(-812 -2028)" fill="none"
                     fill-rule="evenodd"/>
            </svg>
            <slot></slot>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'app-brandshape-border',
    props: {
      color: {
        type: String,
        default: 'var(--green)'
      },
      height: {
        type: String,
        default: '48px'
      },
      width: {
        type: String,
        default: '48px'
      }
    }
  }
</script>

<style lang="stylus" scoped>
    ._brandshape-border
        position relative
        width 100%
        height 100%
        overflow hidden
        padding 1px
        justify-content center
        display flex
        &--mask
            position absolute
            top 0
            left 0
            min-height 100%
            min-width 100%
</style>
