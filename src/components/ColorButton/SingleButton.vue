<template>
    <div  class="cy-button cy">
        <button
            :class="[
                // 默认配置样式
                'but-init',
                // 动态样式
                'transparent',
                // 波纹效果类名
                corrs ? 'corrs' : '',
                // 添加背景色
                color,
                // 按钮大小
                size,
                {
                    // 是否为圆角按钮
                    'round': round,
                    // 是否为线框按钮
                    'dehased': dehased,
                    // 是否禁用按钮
                    'disabled': disabled,
                }
            ]"
        >
        <!-- 设置插槽，并进行判断，组件被调用时是否需要使用插槽 -->
        <span v-if="$slots.default"><slot></slot></span>
        </button>
    </div>
</template>

<script>
export default {
    name: 'SingleButton',
    // 使用 prop 自定义属性
    props: {
        // 是否为圆角按钮
        round: Boolean,
        // 是否禁用按钮
        disabled: Boolean,
        // 是否为线框按钮
        dehased: Boolean,
        // 是否给按钮添加波纹效果
        corrs: Boolean,
        // 单背景色选项
        single: {
            type: Number,
            default: 0
        },
        // 按钮大小
        size: {
            type: String
        }
    },
    data(){
        return{
            color: this.single || 0
        }
    },
    created () {
        switch(this.color){
            case 1:
                this.color = "a"
            break;
            case 2:
                this.color = "a1"
            break;
            case 3:
                this.color = "a2"
            break;
            case 4:
                this.color = "a3"
            break;
            case 5:
                this.color = "a4"
            break;
            case 6:
                this.color = "a5"
            break;
            case 7:
                this.color = "a6"
            break;
            case 8:
                this.color = "a7"
            break;
            case 9:
                this.color = "a8"
            break;
            default:
                this.color = "tomato"
        }
    },
    methods: {
      // 生成波纹
      createRipple(event){
        // 获取当前按钮
        const button = event.currentTarget
        // 创建 span 标签，用作波纹效果
        const circle = document.createElement("span")
        // 获取 button 可视区域的最大宽或高
        const diameter = Math.max(button.clientWidth, button.clientHeight)
        // 设置 span 为按钮的一半
        circle.style.width = diameter / 2 + 'px'
        circle.style.height = diameter / 2 + 'px'
        // 设置波纹的 left 位置
        circle.style.left = diameter / 4 + 'px'
        // 设置波纹的 top 位置
        circle.style.top = -5 + 'px'
        // 给 span 标签添加类名 ripple
        circle.classList.add("ripple")
        // 获取类名为 ripple 的标签
        const ripple = button.getElementsByClassName("ripple")[0]
        // 判断是否存在
        if (ripple) {
            // 存在则移除
            ripple.remove()
        }
        // 不存在则添加
        button.appendChild(circle)
      },
      // 绑定按钮
      corr(){
        let button = document.querySelectorAll('.corrs')
        for(let i = 0; i < button.length; i++){
          let corr = button[i]
          corr.addEventListener("click", this.createRipple)
        }
      }
    },
    mounted () {
      this.corr()
    }
}
</script>

<style scoped>
    /* 引入配置 CSS */
    @import url('../but-init-style/but-init.css');
    /* 引入属性 */
    @import url('../but-init-style/but-attr.css');
    /* 按钮波纹效果 */
    @import url('../but-init-style/but-corr.css');
    /* 引入单色背景 */
    @import url('./but-style/SingleBackground.css');
</style>