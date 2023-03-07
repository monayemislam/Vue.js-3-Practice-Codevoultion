<template>
<h2 :id="headingId">Heading</h2>
<button :disabled="isDisabled">Bind</button>
<h2 class="underline">underline Text</h2>
<h2 class="underline" :class="status">Status</h2>
<h2 :class="isPromoted && 'promoted'">Promoted Movied</h2>
<h2 :class="isSoldout ? 'sold-out' : 'new' ">Sold Out</h2>
<h2 :class="['new','promoted']">Newly Promoted</h2>
<h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array Conditional movie</h2>

<h2 :class="{
  promoted: isPromoted,
  new: !isSoldout,
  'sold-out': isSoldout
}">Object Conditional Movie
</h2>

<h2 :style="{
  color: highlightColor,
  // 'font-size': headerSize + 'px',
  fontSize: headerSize + 'px',
  padding: 20,
}">Inline Style</h2>

<h2 :style="headerStyleObject">Inline Style</h2>

<h2 :style="[baseStyleObject, successStyleObject]">Inline Style</h2>

<h2 :style="[baseStyleObject, dangerStyleObject]">Inline Style</h2>

</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      headingId: "heading",
      isDisabled: true,
      status: 'danger',
      isPromoted: false,
      isSoldout: true,
      headerSize: 50,
      highlightColor: 'orange',
      headerStyleObject:{
        color: 'orange',
        fontSize: '50px',
        padding: '20px',
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green'
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred'
      },
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}
.new{
  color: olivedrab;
}
.sold-out{
  color: #f00;
}
</style>
