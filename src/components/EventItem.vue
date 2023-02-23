<template>
  <article class="item-container">
    <div class="item-header">
      <span class="header-text">{{ title }}</span>
      <span class="header-label">{{eventType}}</span>
    </div>
    <div class="item-content">
       <div>{{ content }}</div>
       <div class="content-item">
         <span>Date:</span>
         <span>{{date}}</span>
       </div>
      <div class="content-item">
        <span>Status:</span>
        <span class="active" :class="{  completed: isCompleted }">{{status}}</span>
      </div>

    </div>
    <div class="item-actions">
       <a href="#" class="button">Open</a>
    </div>
  </article>
</template>

<script>

export default {
  name: "EventItem",
  props : ['title', 'content', 'type', 'date','status'],
  computed : {
    eventType : function() {
      switch (this.type) {
        case 'quiz':
          return 'Q';
        default:
          return 'N/A'
      }
    },
    isCompleted : function() {
      return this.status !== 'Active';
    }
  }


}
</script>

<style scoped>
:root {
  --cardWidth: 240px;
  --cardHeight: 240px;
  --cardMargin: 16px;
}
.item-container {
  /*width: var(--cardWidth);
  height: var(--cardHeight);
  margin: var(--cardMargin);*/
  flex: 0 0 20em;

  border: 1px solid #ccc;
  border-radius: 2px;
  background: #fff;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-content: start;
  margin: 5px;

  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;

}
.item-header {
  flex: 10;
  display: flex;
  justify-content: space-between;
  border-bottom: lightgray 1px solid;


}
.item-header .header-text {
  flex: 12;
  text-align: center;
  font-weight: bold;
}
.item-header .header-label {
  flex :1;
  background-color: darkgreen;
  color: #cccccc;
  text-align: center;
  font-weight: bold;


}
.item-content {
  flex : 4;
  display: flex;
  flex-direction: column;
  border-bottom: lightgray 1px solid;
  margin : 2px
}

.content-item {
  display: flex;
  justify-content: space-between;
  padding: 2px;

}
.content-item .active {
  color: green;
}
.content-item .completed {
  color: red;
}
.item-actions {
  flex : 1;
  display: flex;
  margin : 2px;
  justify-content: center;

}

a.button {
  color : #8bbdbb;
  padding: 2px 5px;
  text-decoration: none;
  text-transform: uppercase;
  font-size: smaller;
}

a.button:hover {

  cursor: pointer;
  background-color: #8bbdbb;
  color: white;
}

a.button:active {
  background-color: black;
}

a.button:visited {
  background-color: #ccc;
}
</style>