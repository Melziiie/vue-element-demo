<template>
  <div class="about">
    <el-row :gutter="8">
      <el-col :span="12" v-for="(o) in 6" :key="o">
        <el-card :body-style="{ padding: '0px' }">
          <img src="https://picsum.photos/235/236" class="image">
          <div style="padding: 10px;">
            <span class="desc">Yummy hamburger</span>
            <div class="bottom clearfix">
              <span class="price">$40</span>
              <el-button type="text" class="button">Read More..</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<style>
.el-row{
  display:flex;
  flex-wrap:wrap;
  justify-content: center;
}
.el-col{
  margin-top:20px;
}
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  } 
  .price {
    padding: 0;
    float: left;
  }
  .button {
    font-size:8px;
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
</style>


