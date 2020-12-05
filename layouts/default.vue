<template>
  <div>
    <Nuxt />
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
font-family: 'Nunito', sans-serif;

}

.top_form input,
.bottom_form input
{
  // border-bottom: 1px solid #000 !important;
  border-color: #000 !important;
  &:focus{
 border-bottom: 1px solid #000 !important;
  border-color: #000 !important;

  }
  &:active{
    border-color: #000 !important;
  }
}
</style>
