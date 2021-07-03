<template>
    <div class="nav">
        <div class="navbar">
            <img src="../assets/img/logo.png" class="logo"/>
                <nav>
                    <ul :class="{height: isActive}">
                        <li><a href="">Game Cotrollers</a></li>
                        <li><a href="">VR Accessories</a></li>
                        <li><a href="">Media Remotes</a></li>
                        <li><a href="">Others</a></li>
                    </ul>
                </nav>
            <img src="../assets/img/menu.png" class="menu-icon" @click="isActive = !isActive"/>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            isActive: false,
        }
    }
}
</script>
<style lang="scss" scoped>
.navbar{
    width: 100%;
    display: flex;
    align-items: center;
}

.logo{
    width: 50px;
    cursor: pointer;
    margin: 30px 0;
}

.menu-icon{
    width: 25px;
    cursor: pointer;
    display: none;
}

nav{
    flex: 1;
    text-align: right;
    ul{
        li{
            list-style: none;
            display: inline-block;
            margin-right: 30px;
            a{
                text-decoration: none;
                color: #000;
                font-size: 14px;
                &:hover{
                    color: #ff5ea2;
                }
            }
        }
    }
}

@media screen and (max-width:780px){
    .nav{
        margin-bottom: 130px;
    }
    nav{
        ul{
            transition: 0.6s; 
            height: 0; //nesessary
            // ⬇︎ once you click the icon
            // height:140px; in .height
            background: linear-gradient(#ff54a2, #ff575a);
            width: 100%;
            position: absolute;
            top: 75px;
            right: 0;
            z-index: 2;
            li{
                display: none; //not that nesessary
                // ⬇︎ once you click the icon
                // display: block;
                margin-top: 10px;
                margin-bottom: 10px;
                a{
                    color: #fff;
                    &:hover{
                        color: #e0d9d9;
                    }
                }
            }
        }
    }
    .menu-icon{
        display: block;
    }
    
    .height{
        height: 140px;
        li{
            display: block;
        }
    }
}
</style>