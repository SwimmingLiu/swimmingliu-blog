---
hidemeta: true
---

<style>

    @media screen and (max-width: 768px){
        .container{
            margin-top: 50px;
            display:flex;
            flex-direction: column;
            justify-content: center;
            align-items:center;
            width:100%;
        }
        .leftBox{
            display: flex; 
            flex-direction: column;
            justify-content: center;
            align-items: center; 
            
        }
        .rightBox{
            margin-top:30px;
            box-sizing: border-box;
            padding: 10px;
            display:flex;
            flex-direction: column;
            justify-content: flex-start;
        }
        .introImg{
            border-radius: 50%;
            box-sizing: border-box;
            width: 25vh;
            height: 25vh ;
            background-image: url("https://oss.swimmingliu.cn/SwimmingLiu-08f19bdf2935.png");
            background-size:100% 100%;
        }
        .introBox{
            display: flex; 
            flex-direction: column;
            justify-content: space-around;
            
            font-size: 15px;
            font-family: 'Times New Roman', Times, serif;
        }
        .introText{
            color: transparent;
        }
        .specialSpan{
            font-weight: bold;
            font-size: 15px; 
            color: black;
        }
    }
    @media screen and (min-width: 768px){

        .container{
            margin-top: 100px;
            display:flex;
            flex-direction: row;
            justify-content: center;
            width:100%;
        }
        .leftBox{
            width: 30%;
            display: flex; 
            flex-direction: column;
            justify-content: center;
            align-items: center; 
            
        }
        .introImg{
            border-radius: 50%;
            box-sizing: border-box;
            width: 16vw;
            height: 16vw;
            background-image: url("https://oss.swimmingliu.cn/SwimmingLiu-08f19bdf2935.png");
            background-size:100% 100%;
        }
        .introImg:hover{
            animation: rotate 1s linear infinite;
        }
        @keyframes rotate {
            0% {
                transform: rotate(0deg);
                /*从0度开始*/
            }
            100% {
                transform: rotate(360deg);
                /*360度结束*/
            }
        }

        .rightBox{
            margin-left:30px;
            box-sizing: border-box;
            padding: 10px;
            width:70%;
            display:flex;
            flex-direction: column;
            justify-content: flex-start;
        }
        .introBox{
            font-size: 18px;
            font-family: 'Times New Roman', Times, serif;
        }
        .introText{
            color: transparent;
        }
        .specialSpan{
            font-weight: bold;
            font-size: 20px; 
            color: black;
        }
    }
    </style>
    
<div class="container">
            <div class="leftBox">
                  <div class="introImg"></div>
            </div>
            <div class="rightBox">
                <div class="introBox">
                    <div>
                        <span>Name:</span>
                        <span class="specialSpan"> 𝓢𝔀𝓲𝓶𝓶𝓲𝓷𝓰𝓛𝓲𝓾 👨🏻‍🎓</span>
                    </div>
                    <div>
                        <span>Age:</span>
                        <span class="specialSpan"> 𝟮𝟯 </span>Years Old 👦🏻
                    </div>
                    <div>
                        <span>Country:</span>
                        <span class="specialSpan"> 𝓒𝓱𝓲𝓷𝓪 🇨🇳</span>
                    </div>
                    <div>
                        <span>Education:</span> Study in <span class="specialSpan">𝓩𝓢𝓣𝓤 🏫</span>
                    </div>
                    <div>
                        <span class="introText">Education:</span> Majoring <span class="specialSpan">𝓒𝓸𝓶𝓹𝓾𝓽𝓮𝓻 𝓢𝓬𝓲𝓮𝓷𝓬𝓮 💻</span>
                    </div>
                    <div>
                        Exploring the <span class="specialSpan">𝓦𝓸𝓻𝓵𝓭</span> with <span class="specialSpan">𝓒𝓸𝓶𝓹𝓾𝓽𝓮𝓻 𝓥𝓲𝓼𝓲𝓸𝓷 🌎</span> 
                    </div>
                </div>
            </div>
</div>
    
<script>
    // 定义一个函数，根据 body 的 class 设置 span 的颜色
    function setSpanColor() {
    const bodyClass = document.body.classList;
    const introBox = document.querySelector('.introBox');
    const spanElements = introBox.querySelectorAll('span');

    if (bodyClass.contains('dark')) {
        spanElements.forEach(spanElement => {
        spanElement.style.color = 'white';
        });
    } else {
        spanElements.forEach(spanElement => {
        spanElement.style.color = 'black';
        });
    }
    }

    // 调用函数以确保初始状态正确
    setSpanColor();

    // 开始观察 body 元素的 classList 变化
    const bodyObserver = new MutationObserver(mutations => {
    mutations.forEach(mutation => {
        if (mutation.type === 'attributes' && mutation.attributeName === 'class') {
        setSpanColor();
        }
    });
    });

    bodyObserver.observe(document.body, { attributes: true });

</script>
    
