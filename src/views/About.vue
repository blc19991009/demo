<template>
  <div>
    <!--单行文本溢出  -->
    <h2>单行文本溢出</h2>
    <div class="box1">
      <ul>
        <li title="全部内容展示：文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1">
          文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1文本内容1
        </li>   
      </ul>
    </div>

    <!-- 多行文本溢出 -->
    <h2>多行文本溢出</h2>
    <div class="box2">
      <ul>
        <li title="全部内容展示： 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2">
          文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2 文本内容2
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.box1 ul {
  width: 200px;
}

.box1 ul li {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.box2 ul {
  width: 200px;
}

.box2 ul li {
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
}
</style>