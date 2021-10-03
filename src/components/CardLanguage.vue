<template>
    <li class="languages__item">
        <i 
            class="languages__item--icon" 
            :style="'--hoverColor:' + hoverColor "
            :class="icon"    
        ></i>
    </li>
</template>

<script>
export default {
    props: [
        'lang'
    ],
    computed: {
        hoverColor: function () {
            let color = "#fff"

            // REFACTOR THIS SWITCH!

            switch (this.lang) {
                case "html":
                    color = "#F65314";
                    break;
                case "css":
                    color = "#0f5da8";
                    break;
                case "react":
                    color = "#2c80ec";
                    break;
                case "js":
                    color = "#dc901e";
                    break;
                case "vue":
                    color = "#42b883";
                    break;
                case "java":
                    color = "#FFA518";
                    break;
                case "sql":
                    color = "#7CBB00";
                    break;
                default:
                    break;
            }
            return color;
        },
        icon: function(){
            let icon = "fas fa-bug"
            switch (this.lang) {
                case "html":
                    icon = "fab fa-html5";
                    break;
                case "css":
                    icon = "fab fa-css3-alt";
                    break;
                case "react":
                    icon = "fab fa-react";
                    break;
                case "js":
                    icon = "fab fa-js-square";
                    break;
                case "vue":
                    icon = "fab fa-vuejs";
                    break;
                case "java":
                    icon = "fab fa-java";
                    break;
                case "sql":
                    icon = "fas fa-database";
                    break;
                default:
                    break;
            }
            return icon;
        }
    }
}
</script>

<style scoped>
.languages__item{
    margin: 5px;    
}
.languages__item--icon{
    width: 20px;
    font-size: 26px;
    color: #fff;
    transform: rotate(180deg);
    cursor: help;
}
.languages__item--icon:hover{
    color: var(--hoverColor);
}
</style>