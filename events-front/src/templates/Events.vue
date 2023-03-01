<template>
  <Layout>
    <h1>
      {{$page.event.title}}
    </h1>
    <img :src="'https://cdn.vuetifyjs.com/images/cards/docks.jpg'" />
    <p>{{$page.event.description}}</p>
  </Layout>
</template>

<page-query>
query {
  event: events(id: "1") {
    id 
    title
    description
    duration
    price
    date
  }
}
</page-query>

<script>
export default {
  metaInfo() {
    return {
      title: this.$page.event.title
    }
  }
}
</script>