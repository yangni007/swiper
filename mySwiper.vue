<template>

  <div  class='box' >
      <ul :style='ul_width'>
          <li :style='gap_li' v-for='(item, index) in List' :key='index'>
            <img :src='item.src'/>
            <slot :text='item.content'></slot>
          </li>
      </ul>
  </div>

</template>
<script>
export default {
  data () {
    return {
      List : this.dataList,
      default_gap: 10,
      default_width: 30,
      default_height:50,
    }
  },
  props: ['gap','width', 'dataList', 'height'],
  computed: {
    gap_li(){
      var str= 'width:'+(this.width||this.default_width)+'px;'
                +'height:'+( this.height|| this.default_height)
                +'px;margin-right:'+(this.gap||this.default_gap)+'px';
      return str;
    },
    
    ul_width(){

      var str = 'width:'+this.List.length*(this.width+(this.gap||this.default_gap))+'px;';
      return str;
    }
  },
 mounted(){
 
 }
}
</script>
<style lang='less' scoped>
.box{
  overflow: auto;

  ul{
    display: inline-block;
 
    list-style: none;

    li{
      float: left;
      img{
        width:100%;
        height:70%;
      }
    }
  }
}
</style>
