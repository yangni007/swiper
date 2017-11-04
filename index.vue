<template>
 
  <div>
      <mySwiper width='100' height='150' :dataList='List'>
          <div slot-scope='props' class='text-center'>
            <p >{{props["text"].name}}</p>
            <p class="font-fade">{{props["text"].inmovie}}</p>
          </div>
      </mySwiper>
  </div>
  </transition>

<script>

import mySwiper from './mySwiper'
export default {
  data () {
    return {
      List: [
      {
        src: 'https://static.vux.li/demo/3.jpg',
        content: {
          name: '张某某',
          inmovie: '导演'
        }
        
      },
      {
        src: 'https://static.vux.li/demo/3.jpg',
        content: {
          name: '赵丽颖',
          inmovie:'兰芳'
        }
      },
      {
        src: 'https://static.vux.li/demo/3.jpg',
        content: {
          name: '郭富城',
          inmovie:'林翔'
        }
      },
      {
        src: 'https://static.vux.li/demo/3.jpg',
        content: {
          name: '张翰',
          inmovie:'梁栋'
        }
        
      },
        ]
    }
  },
 mounted(){
  
 }
}
</script>
<style lang='less' scoped>
 .text-center {
  text-align: center ;
}
.font-fade {
  color: #999 ;
}
</style>
