<template>
  <div class="row">
    <div class="col-md-5">
      <div class="description">
        <h2>PS4 V2<br/>Dualshock 4</h2>
        <h3>Wireless Controller for PlayStation 4</h3>
        <p>(Compatible/Generic)</p>
        <h4>$32.50</h4>
        <button type="button">Buy Now<img src="../assets/img/arrow.png" /></button>
      </div>
    </div>
        
    <div class="col-md-7">
      <img src="../assets/img/controller.png" class="controller" />
      <div class="color-box"></div>
      <div class="add-btn">
        <img src="../assets/img/add.png"/>
        <p><small>Add to cart</small></p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
.row{
  justify-content: space-between;
  align-items: center;
  margin: 100px 0;
}

.description{
  position: relative;
  margin-left: 50px;
  margin-bottom: 100px;
  &::after{
    content: '';
    width: 10px;
    height: 57%;
    background: linear-gradient(#ff469f, #ff6062);
    position: absolute;
    left: -20px;
    top: 0;
  }
  h2{
    font-size: 54px;
  }
  h3{
    font-size: 30px;
    color: #707070;
    font-weight: 100;
    margin:20px 0 10px;
  }
  p{
    font-size: 16px;
    color: #b7b7b7;
    font-weight: 100;
  }
  h4{
    margin: 30px 0;
    font-size: 20px;
  }
}

.col-md-7{
  padding: 0;
  align-items: center;
  img{
    width: 90%;
  }
}

button{
  width: 140px;
  border: 0;
  padding: 12px 10px;
  outline: none;
  color: #fff;
  background: linear-gradient(to right, #fb5283, #ff3527);
  border-radius: 6px;
  cursor: pointer;
  transition: width 0.9s;
  img{
    width: 30px;
    display: none;
  }
  &:hover{
    width: 160px;
    align-items: center;
    justify-content: center;
    img{
      display: inline;
    }
  }
}

.color-box{
  position: absolute;
  right: 0;
  top: 0;
  background: linear-gradient(#ff54a2, #ff575a);
  border-radius: 20px 0 0 20px;
  height: 100%;
  width: 80%;
  z-index: -1;
}

.add-btn{
  text-align: center;
  transform: translate(40%,-300%);
  color: #fff;
  cursor: pointer;
  img{
    width: 35px;
    margin-bottom: 5px;
  }
}
</style>