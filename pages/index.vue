<template>
<!-- this is the parent div  -->
<!-- find out how to move a div using a shortcut -- move a line -->
<!-- To center content in a grid use justify-times-center -->
<!-- use underscore to make page dynamic -->
<div class="h-screen">
  <div class="h-2/5 text-white bg-gray-900">

    <h1 class="text-xl ">Hello world</h1>
    <!-- tells us what the name of the path is global item get injected into the data gives you path -->
     path : {{ $route.path }}
  </div>


  <div class="pt-10 grid grid-cols-3 gap-10 justify-items-center h-48">
    <!-- the : makes everying inside in the quotes to javascript -- look at key for example -- can also use index in th v for loop -->
    <div v-for="(pic,i) in pics" :key="i" class="bg-red-500">
      <img :src="pic" alt="">
    </div>
  </div>
</div>

</template>

<script>
// state of the component is here 
  export default {
    data : () => {
      // default data
      return {
        message : 'hello world',
        pics: [
          'https://images.unsplash.com/photo-1499578124509-1611b77778c8?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=2110&q=80',
          'https://images.unsplash.com/photo-1514944152559-a103040c7f16?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=2102&q=80',
          'https://images.unsplash.com/photo-1512987415479-85f370bca602?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=2100&q=80'
        ]
      }
    }
  }
</script>
