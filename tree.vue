<template>
  <li>
    <div
      :class="{bold: isFolder}"
      @click="toggle"
      @dblclick="changeType">
      {{ model.name }}
      <span v-if="isFolder">[{{ open ? '-' : '+' }}]</span>
    </div>
    <ul v-show="open" v-if="isFolder">
      <item
        class="item"
        v-for="(model, index) in model.children"
        :key="index"
        :model="model">
      </item>
      <li class="add" @click="addChild">+</li>
    </ul>
  </li>
  
  <ul id="demo">
  <item
    class="item"
    :model="treeData">
  </item>
</ul>
</template>

<script type="text/javascript">
  export default {
    name: 'tree items',
    //     data(){
    //       return{
    //       data : {
    //   name: 'My Tree',
    //   children: [
    //     { name: 'hello' },
    //     { name: 'wat' },
    //     {
    //       name: 'child folder',
    //       children: [
    //         {
    //           name: 'child folder',
    //           children: [
    //             { name: 'hello' },
    //             { name: 'wat' }
    //           ]
    //         },
    //         { name: 'hello' },
    //         { name: 'wat' },
    //         {
    //           name: 'child folder',
    //           children: [
    //             { name: 'hello' },
    //             { name: 'wat' }
    //           ]
    //         }
    //       ]
    //     }
    //   ]
    // }
    //       }
    //     }
    props: {
      model: Object
    },
    data: function() {
      return {
        open: false
      }
    },
    computed: {
      isFolder: function() {
        return this.model.children &&
          this.model.children.length
      }
    },
    methods: {
      toggle: function() {
        if (this.isFolder) {
          this.open = !this.open
        }
      },
      changeType: function() {
        if (!this.isFolder) {
          Vue.set(this.model, 'children', [])
          this.addChild()
          this.open = true
        }
      },
      addChild: function() {
        this.model.children.push({
          name: 'new stuff'
        })
      }
    }

  }
</script>
