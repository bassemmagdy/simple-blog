<template>
  <div class="col-sm6 col-md-4 col-lg-3">
    <div class="panel-body quote">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.panel-body {
  font-family: 'Arizone', cursive;
  font-size: 24px;
  color: #6e6e6e;
}
.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
}
</style>
