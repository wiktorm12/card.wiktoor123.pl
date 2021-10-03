<template>
    <li class="list__item">
        <i class="list__item__icon"
            :class="iconClass"
        ></i>
        <p class="list__item__value">
            {{ item.value }}
        </p>
    </li>
</template>

<script>
export default {
    computed: {
        iconClass: function(){
            let iconClass = "";
            switch (this.item.type) {
                case "location":
                    iconClass = "fas fa-map-marker-alt"
                    break;
                case "github":
                    iconClass = "fab fa-github"
                    break;
                case "mail":
                    iconClass = "far fa-envelope"
                    break;
                case "page":
                    iconClass = "fas fa-globe-americas"
                    break;
                case "phone":
                    iconClass = "fas fa-phone"
                    break;
                default:
                    iconClass = "fas fa-bug"
                    break;
            }
            return iconClass
        }
    },
    props: [
        'item'
    ]
}
</script>

<style scoped>
.list__item{
    display: flex;
    margin: 5px 20px;
}
.list__item__value{
    margin-left: 10px;
}
.list__item__icon{
    width: 20px;
}
.list__item__value--nolink:hover {
    transform: scale(1.01);
    letter-spacing: 1px;
}
.list__item__value--nolink{
    color: #fff;
    transition: .5s;
    text-decoration: none;
}
</style>