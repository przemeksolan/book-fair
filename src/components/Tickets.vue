<template>
  <div class="read_l">
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-text" class="span-third span-full-t text-clip box">Text</label>
      <input class="input" type="text" id="e-text" placeholder="Just text">
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-fav-fruit" class="span-third span-full-t text-clip box">Text with datalist</label>
      <input class="input" type="text" list="fruits" id="e-fav-fruit" placeholder="data-list example">
      <datalist id="fruits">
        <option value="Apple"></option>
        <option value="Orange"></option>
        <option value="Peach"></option>
        <option value="Melon"></option>
        <option value="Strawberry"></option>
      </datalist>
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-text-readonly" class="span-third span-full-t text-clip box">Text:readonly</label>
      <input class="input" type="text" id="e-text-readonly" value="Only to read." readonly>
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-text-disabled" class="span-third span-full-t text-clip box">Text:disabled</label>
      <input class="input" type="text" id="e-text-disabled" value="Disabled." disabled>
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-password" class="span-third span-full-t text-clip box">Password</label>
      <input class="input" type="password" id="e-password" placeholder="•••••••••••">
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-email" class="required span-third span-full-t text-clip box">Email</label>
      <input class="input" type="email" id="e-email" name="email" required>
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-number" class="span-third span-full-t text-clip box">Number</label>
      <input class="input" type="number" name="number" id="e-number" value="42">
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-tel" class="span-third span-full-t text-clip box">Tel</label>
      <input class="input" type="tel" name="tel" id="e-tel">
    </div>
    <div class="flex wrap-no gap-no collapse-t">
      <label for="e-url" class="span-third span-full-t text-clip box">URL</label>
      <input class="input" type="url" name="url" id="e-url" placeholder="https://www.fortrabbit.com">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
