!<template>
    <section class="title">
          <h1 class="title__name">
              <span class="title__name__first">
                  {{ name }}
              </span>
              <span class="title__name__last">
                    {{ surname }}
              </span>
          </h1>
          <h2 class="title__position">
                {{ position }}
          </h2>
      </section>
</template>

<script>
export default {
    props: [
        'name', 'surname', 'position'
    ]
}
</script>

<style>
.card .title{
    position: absolute;
    left: 30px;
    top: 15px;
    color: #fff;
}
.card .title__name{
    font-size: 25px;
}
.card .title__position{
    font-size: 15px;
    font-weight: 300;
}
.card .title__name__first{
    margin-right: 7px;
}
</style>