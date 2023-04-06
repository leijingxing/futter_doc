# vue开发
## 1. vue的生命周期
```javascript
new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue.js!'
  },
  beforeCreate: function () {
    console.log('beforeCreate')
  },
  created: function () {
    console.log('created')
  },
  beforeMount: function () {
    console.log('beforeMount')
  },
  mounted: function () {
    console.log('mounted')
  },
  beforeUpdate: function () {
    console.log('beforeUpdate')
  },
  updated: function () {
    console.log('updated')
  },
  beforeDestroy: function () {
    console.log('beforeDestroy')
  },
  destroyed: function () {
    console.log('destroyed')
  }
})
```

## 2. vue的数据绑定

```javascript
<div id="app">
  <p>{{ message }}</p>
  <p v-text="message"></p>
  <p v-html="message"></p>
  <p v-bind:title="message"></p>
  <p v-once>{{ message }}</p>
</div>
```

## 3. vue的指令

```javascript
<div id="app">
  <p v-if="seen">现在你看到我了</p>
  <p v-else>现在你看不到我了</p>
  <p v-show="seen">现在你看到我了</p>
  <p v-show="!seen">现在你看不到我了</p>
  <p v-for="item in items">{{ item.message }}</p>
  <p v-on:click="reverseMessage">逆转消息</p>
</div>
```

## 4. vue的计算属性

```javascript
<div id="app">
  <p>原始消息：{{ message }}</p>
  <p>计算属性：{{ reversedMessage }}</p>
  <p>方法：{{ reversedMessage()}}</p>
</div>
```

## 5. vue的侦听器

```javascript
<div id="app">
  <p>原始消息：{{ message }}</p>
  <p>计算属性：{{ reversedMessage }}</p>
  <p>方法：{{ reversedMessage()}}</p>
</div>
```

## 6. vue的class和style绑定

```javascript
<div id="app">
  <p v-bind:class="{ active: isActive }">class绑定</p>
  <p v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }">style绑定</p>

    <p v-bind:class="[activeClass, errorClass]">class绑定</p>
    <p v-bind:class="[isActive ? activeClass : '', errorClass]">class绑定</p>
    <p v-bind:class="[{ active: isActive }, errorClass]">class绑定</p>
    <p v-bind:style="[baseStyles, overridingStyles]">style绑定</p>
</div>
```

## 7. vue的条件渲染

```javascript
<div id="app">
  <p v-if="type === 'A'">A</p>
  <p v-else-if="type === 'B'">B</p>
  <p v-else-if="type === 'C'">C</p>
  <p v-else>Not A/B/C</p>
  <p v-show="type === 'A'">A</p>
  <p v-show="type === 'B'">B</p>
  <p v-show="type === 'C'">C</p>
  <p v-show="type !== 'A' && type !== 'B' && type !== 'C'">Not A/B/C</p>
</div>
```

## 8. vue的列表渲染

```javascript
<div id="app">
  <p v-for="item in items">{{ item.message }}</p>
  <p v-for="(item, index) in items">{{ index }} - {{ item.message }}</p>
  <p v-for="(value, key, index) in object">{{ index }} - {{ key }} - {{ value }}</p>
  <p v-for="n in 10">{{ n }}</p>
  <p v-for="(item, index) in 10">{{ index }} - {{ item }}</p>
</div>
```

## 9. vue的事件处理

```javascript
<div id="app">
  <p v-on:click="greet">Greet</p>
  <p v-on:click="say('hi')">Say hi</p>
  <p v-on:click="warn('Form cannot be submitted yet.', $event)">Submit</p>
  <p v-on:click="say('hi', $event)">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5', 'arg6')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5', 'arg6', 'arg7')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5', 'arg6', 'arg7', 'arg8')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5', 'arg6', 'arg7', 'arg8', 'arg9')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2', 'arg3', 'arg4', 'arg5', 'arg6', 'arg7', 'arg8', 'arg9', 'arg10')">Say hi</p>
  <p v-on:click="say('hi', $event, 'arg1', 'arg2, 'arg3', 'arg4', 'arg5', 'arg6', 'arg7', 'arg8', 'arg9', 'arg10', 'arg11')">Say hi</p>
    <p v-on:click="say('hi', $event, 'arg1', 'arg2, 'arg3', 'arg4', 'arg5', 'arg6', 'arg7', 'arg8', 'arg9', 'arg10', 'arg11', 'arg12')">Say hi</p>
</div>
```

## 10. vue的表单输入绑定

```javascript
<div id="app">
  <p>
    <input type="text" v-model="message">
    {{ message }}
  </p>
  <p>
    <input type="checkbox" id="checkbox" v-model="checked">
    <label for="checkbox">{{ checked }}</label>
  </p>
  <p>
    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
    <label for="jack">Jack</label>
    <input type="checkbox" id="john" value="John" v-model="checkedNames">
    <label for="john">John</label>
    <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
    <label for="mike">Mike</label>
    <br>
    <span>Checked names: {{ checkedNames }}</span>
  </p>
  <p>
    <input type="radio" id="one" value="One" v-model="picked">
    <label for="one">One</label>
    <br>
    <input type="radio" id="two" value="Two" v-model="picked">
    <label for="two">Two</label>
    <br>
    <span>Picked: {{ picked }}</span>
  </p>
  <p>
    <select v-model="selected">
      <option disabled value="">请选择</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
    <span>Selected: {{ selected }}</span>
  </p>
  <p>
    <select v-model="selected" multiple>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
    <br>
    <span>Selected: {{ selected }}</span>
  </p>
</div>
```

## 11. vue的组件

```javascript
<div id="app">
  <my-component></my-component>
</div>
```

## 12. vue的组件通信

```javascript
<div id="app">
  <my-component></my-component>
</div>
```