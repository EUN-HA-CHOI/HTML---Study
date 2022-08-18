### css3 : animation4_favebook_emoji  

* 완성 [animation_이모티콘](http://127.0.0.1:5500/facebook_emoji.html)

```css
 <style>
   body {
     text-align: center;
     margin: 80px auto 0;
   }
   .emoji {
     position: relative;
     display: inline-block;
     width: 120px;
     height: 120px;
     border-radius: 50%;
     margin: 15px 15px 40px;
     background: #ffda6a;
   }
   .emoji:after {
     content: "Emoji";
     position: absolute;
     bottom: -40px;
     left: calc(50% - 30%);
     width: 60px;
     font-size: 18px;
     color: #8a8a8a;
   }
   
   /*position:absolute는 margin:0 auto 안된다.
   중앙에 위치 시키는 방법
   1.position:absolute;left:calc(50% - 가로 1/2px); top:calc(50% - 세로 1/2px)
   2.position:absolute;left:50%top:50%; margin-left: -가로1/2px;margin-top:-세
   3.position:absolute;left:50%top:50%; transform:translate3d(-50%,-50%,0);
   */  
   /*1.emoji_like*/
   .emoji_like {background: #548dff;}
   .emoji_like:after {content: 'Like';}
     
   .emoji_like .emoji_hand {
     position: absolute;
     left: 25px;
     bottom: 30px;
     width: 20px;
     height: 40px;
     background: #fff;
     border-radius: 5px;
     animation: hands-up 2s linear 0s infinite;
   }
   @keyframes hands-up {
     25%{transform: rotate(15deg);}
     50%{transform: rotate(-15deg) translateY(-10px);}
     75%,100% {transform: rotate(0deg);}
   }
   .emoji_like .emoji_hand:before {
     content: "";
     position: absolute;
     left: 25px;
     bottom: 5px;
     width: 40px;
     height: 10px;
     background: #fff;
     border-radius: 2px 10px 10px 2px;
     box-shadow: 1px -9px 0 1px #fff,
     2px -19px 0 2px #fff,
     3px -29px 0 3px #fff;
   }
   .emoji_like .emoji_thumb {
     position: absolute;
     right: -25px;
     top: -25px;
     border-bottom: 20px solid #fff;
     border-left: 20px solid transparent;
     transform: rotate(5deg);
     transform-origin: 0 100%;
     animation: thumbs-up 2s linear 0s infinite;
   }
   @keyframes thumbs-up {
     25% {transform: rotate(20deg);}
     50%, 100%{transform:rotate(5deg)}
   }
   .emoji_like .emoji_thumb:before {
     content: '';
     position: absolute;
     left: -9.7px;
     top:-9px;
     width: 10px;
     height: 12px;
     background: #fff;
     border-radius: 50% 50% 0 0;
     box-shadow: -1px 4px 0 -1px #fff;
     transform: rotate(-14deg);
     transform-origin: 100% 100%;
   }
   
   /*2.emoji_love*/
   .emoji_love {background: #f55064;}
   .emoji_love:after {content: "Love";}
   .emoji_love .emoji_heart {
     position: absolute;
     left: 50%;
     top: 50%;
     margin-left: -40px;
     margin-top: -40px;
     width: 80px;
     height: 80px;
     /*border: 1px solid #000;*/
     animation: heart-beat 1s linear infinite alternate ;
   }
   @keyframes heart-beat {
     25%{transform: scale(1.1);}
     75%{transform: scale(0.6);}
   }
   
   .emoji_heart:before,.emoji_heart:after {
     content: '';
     position: absolute;
     left: 50%;
     top: 50%;
     width: 40px;
     height: 64px;
     margin-left: -20px;
     margin-top: -32px;
     background: #fff;
     border-radius: 20px 20px 0 0;
   }
   .emoji_heart:before {
     transform-origin: 0 100%;
     transform:translateX(20px)  rotate(-45deg);
   }
   .emoji_heart:after {
     transform-origin: 100% 100%;
     transform: translateX(-20px)  rotate(45deg);
   }
   /*3.emoji_haha*/
   .emoji_haha:after {
     content: "Haha";
   }
   .emoji_haha .emoji_face{
     position: absolute;
     width: 100%;
     height: inherit;
     animation: haha-face 2s linear infinite normal;
   }
   @keyframes haha-face {
      10%{transform: translateY(25px);}
      20%{transform: translateY(15px);}
      30%{transform: translateY(25px);}
      40%{transform: translateY(15px);}
      50%{transform: translateY(25px);}
      60%{transform: translateY(0);}
      70%{transform: translateY(-10x);}
      80%{transform: translateY(0);}
      90%{transform: translateY(-10px);}
   }
   .emoji_haha .emoji_eyes {
     position: absolute;
     left: 50%;
     top: 35px;
     margin-left: -13px;
     width: 26px;
     height: 6px;
     border-radius: 2px;
     /*background: #fff;*/
     box-shadow: -25px 5px 0 0 #000 ,25px -5px 0 0 #000;
     transform: rotate(20deg);
   }
   
   .emoji_haha .emoji_eyes:after {
     content: "";
     position: absolute;
     left: 0;
     top: 0;
     width: 26px;
     height: 6px;
     border-radius: 2px;
     /*ackground: red;*/
     box-shadow: -25px -5px 0 0 #000,25px 5px 0 0 #000;
     transform: rotate(-40deg);
   }
   .emoji_haha .emoji_mouth {
     overflow: hidden;
     position: absolute;
     left: 50%;
     top: 50%;
     width: 80px;
     height: 40px;
     margin-left: -40px;
     background: #000;
     border-radius: 0 0 40px 40px;
     animation:  haha-mouth 2s linear infinite normal;
   }
   @keyframes haha-mouth {
     10%{transform: scale(0.6);top: 45%;}
     20%{transform:scale(0.8);top: 45%;}
      30%{transform:scale(0.6);top: 45%;}
      40%{transform:scale(0.8);top: 45%;}
      50%{transform:scale(0.6); top:45%;}
      60%{transform:scale(1); top:50%;}
      70%{transform:scale(1.2); top:50%;}
      80%{transform:scale(1);top:50%;}
      90%{transform:scale(1.1);top:50%;}
   }
   
   .emoji_haha .emoji_tongue {
     position: absolute;
     left: 50%;
     bottom: -10px;
     width: 70px;
     height: 30px;
     margin-left: -35px;
     background: #f55064;
     border-radius: 50%;
     }
     /*4.emoji_yay*/
     .emoji_yay:after {content: "Yay";}
     .emoji_yay .emoji_face {
       position: absolute;
       width: 100%;
       height: inherit;
       animation:  yay 1s linear infinite alternate;
     }
     @keyframes yay {
       25% {transform: rotate(-15deg);}
       75% {transform: rotate(15deg);}
     }
     .emoji_yay .emoji_eyebrows{
       position: absolute;
       left: calc(50% - 3px);
       top:30px;
       width: 6px;
       height: 6px;
       border-radius: 50%;
       /*background: #fff;*/
       box-shadow: -6px 0 0 0 #000, -36px 0 0 0 #000000,6px 0 0 0 #000, 36p
     }
     .emoji_yay .emoji_eyebrows:before,.emoji_yay .emoji_eyebrows:after {
       content: "";
       position: absolute;
       left:calc(50% - 18px);
       bottom: 3px;
       width: 36px;
       height: 18px;
       border-radius: 60px 60px 0 0;
       border: 6px solid black;
       border-bottom: 0;
       box-sizing: border-box;
       /*border,padding 값이 실제크기 포함 안됨*/
     }
     .emoji_yay .emoji_eyebrows:before {margin-left: -21px;}
     .emoji_yay .emoji_eyebrows:after{margin-left: 21px;}
     .emoji_yay .emoji_mouth {
       position: absolute;
       left: calc(50% - 3px);
       top:60px;
       width: 6px;
       height: 6px;
       border-radius: 50%;
       /*background: red;*/
       box-shadow: -25px 0 0 0 #000, 25px 0 0 0 #000,
       -35px -2px 30px 10px #D5234C,
       35px -2px 30px 10px #D5234C;
     }
     
     .emoji_yay .emoji_mouth:after {
       content: "";
       position: absolute;
       left: calc(50% - 40px);
       top: -64px;
       width: 80px;
       height: 80px;
       border-radius: 50%;
       border: 6px solid #000;
       box-sizing: border-box;
       border-top-color: transparent ;
       border-right-color: transparent ;
       border-left-color: transparent ;
     }
      /*5.emoji_wow*/
      .emoji_wow:after {content:"";}
      .emoji_wow .emoji_face {
        position: absolute;
        width: 100%;
        height: inherit;
        animation:  wow-face 3s linear 0s infinite;
      }
      @keyframes wow-face {
        15%,25%{transform: rotate(20deg) translateX(-25px);}
        45%,65%{transform: rotate(-20deg) translateX(25px);}
        75%,100%{transform: rotate(0deg) translateX(0);}
      }
      
      .emoji_wow .emoji_eyebrows {
        position: absolute;
        left: calc(50% - 3px);
        width: 6px;
        height: 6px;
        border-radius: 50%;
        /*background: #fff;*/
        box-shadow: -18px 0 0 0 #000,
        -33px 0 0 0 #000,
        18px 0 0 0 #000,
        33px 0 0 0 #000;
        animation: wow-brow 3s linear 0s infinite;
      }
      @keyframes wow-brow {
        15%,65% {top:25px}
        75%,100%,0% {top:15px;}
      }
      
      .emoji_wow .emoji_eyebrows:before, .emoji_wow .emoji_eyebrows:after {
        content: '';
        position: absolute;
        left: calc(50% - 12px);
        top: -3px;
        width: 24px;
        height: 20px;
        border-radius: 50%;
        border: 6px solid #000;
        box-sizing: border-box;
        border-right-color: transparent ;
        border-bottom-color: transparent ;
        border-left-color: transparent ;
       }
       
       .emoji_wow .emoji_eyebrows:before {margin-left: -25px;}
       .emoji_wow .emoji_eyebrows:after  {margin-left: 25px;}
       .emoji_wow .emoji_eyes {
         position: absolute;
         left: calc(50% - 8px);
         width: 16px;
         height: 24px;
         border-radius: 50%;
         /*background: red;*/
         top: 35px;
         box-shadow: 25px 0 0 0 #000,-25px 0 0 0 #000;
       }
 
       .emoji_wow .emoji_tongue {
         position: absolute;
         left: calc(50% - 15px);
         top: 50%;
         width: 30px;
         height: 45px;
         border-radius: 50%;
         background: #000;
         animation:wow-mouth 3s linear 0s infinite ;
       }
       @keyframes wow-mouth {
         10%,30%{width: 20px;height: 20px;left:calc(50% - 10px)}
         10%,30%{width: 30px;height: 40px;left:calc(50% - 15px)}
         75%,100%{height: 50px;}
       }
       
       /*6.emoji_sad*/
       .emoji_sad:after {content:"Sad";}
       .emoji_sad .emoji_face {
        position: absolute;
        width: 100%;
        height: inherit;
        animation:  sad-face 2s ease-in 0s infinite;
      }
      @keyframes sad-face {
        25%,35%{top:-15px}
        55%,95%{top:10px}
        100%,0%{top: 0;}
      }
      .emoji_sad .emoji_eyebrows {
        position: absolute;
        left: calc(50% - 3px);
        top: 35px;
        width: 6px;
        height: 6px;
        border-radius: 50%;
        /*background: #fff;*/
        box-shadow: 
        -40px 9px 0 0 #000,
        -25px 0 0 0 #000,
        25px 0 0 0 #000,
        40px 9px 0 0 #000;
        /*animation: wow-brow 3s linear 0s infinite;*/
        ;
      }
      
      .emoji_sad .emoji_eyebrows:before, .emoji_sad .emoji_eyebrows:after {
        content: '';
        position: absolute;
        left: calc(50% - 15px);
        top: 2px;
        width: 30px;
        height: 20px;
        border-radius: 50%;
        border: 6px solid #000;
        box-sizing: border-box;
        border-right-color: transparent ;
        border-bottom-color: transparent ;
        border-left-color: transparent ;
      }
     
      .emoji_sad .emoji_eyebrows:before {margin-left: -30px; transform: rotate
      .emoji_sad .emoji_eyebrows:after  {margin-left: 30px; transform: rotate(
      .emoji_sad .emoji_eyes {
         position: absolute;
         left: calc(50% - 7px);
         top: 50px;
         width: 14px;
         height: 16px;
         border-radius: 50%;
         /*background: red;*/
         box-shadow: 25px 0 0 0 #000,-25px 0 0 0 #000;
       }
       .emoji_sad .emoji_eyes:after {
           content: '';
           position: absolute;
           width: 12px;
           height: 12px;
           margin-left: 1px;
           background: #548dff;
           border-radius: 0 100% 40% 50% / 0 50% 40% 100%;
           animation: tear-drop 2s ease-in infinite;
         /*border-radius: top-left-x top-right-x bottom-right-x
         bottom-left-x / top-left-y top-right-y bottom-right-y
          bottom-left-y
         */
        }
        @keyframes tear-drop {
       0%,100% {
         display: block;
         left: 35px;
         top: 15px;
         transform: rotate(45deg) scale(0);
       }
       25% {
         display: block;
         left: 35px;
         transform: rotate(45deg) scale(2);
       }
       49.9% {
           display: block;
           left: 35px;
           top: 65px;
           transform: rotate(45deg) scale(0);
       }
       50% {
         display: block;
         left: -35px;
         top: 15px;
         transform: rotate(45deg) scale(0);
       }
       75% {
         display: block;
         left: -35px;
         top: 15px;
         transform: rotate(45deg) scale(2);
       }
       99.9% {
         display: block;
         left: -35px;
         top: 65px;
         transform: rotate(45deg) scale(0)};
       }
       
     .emoji_sad .emoji_mouth {
       position: absolute;
       left: calc(50% - 3px);
       top:90px;
       width: 6px;
       height: 6px;      
       /*background: blue;*/
       border-radius: 50%;
       box-shadow: -18px 0 0 0 #000, 
       18px 0 0 0 #000;
       }
     .emoji_sad .emoji_mouth:after {
       content: "";
       position: absolute;
       left: calc(50% - 30px);
       top: -10px;
       width: 60px;
       height: 80px;
       border-radius: 50%;
       border: 6px solid #000;
       box-sizing: border-box;
       border-right-color: transparent ;
       border-bottom-color: transparent ;
       border-left-color: transparent ;
   
     } 
     
     .emoji_sad .emoji_mouth {
       position: absolute;
       left: calc(50% - 3px);
       top:90px;
       width: 6px;
       height: 6px;
       border-radius: 50%;
       box-shadow: -18px 0 0 0 #000, 18px 0 0 0 #000,
     }
     
     .emoji_sad .emoji_mouth:after {
       content: "";
       position: absolute;
       left: calc(50% - 30px);
       top: -10px;
       width: 60px;
       height: 80px;
       border-radius: 50%;
       border: 6px solid #000;
       box-sizing: border-box;
       border-right-color: transparent ;
       border-bottom-color: transparent ;
       border-left-color: transparent ;
     } 
     /*7.emoji_angry*/
     .emoji_angry:after {
       content: 'angray';
     }
     .emoji_angry {
       background: linear-gradient(to bottom, #D5234C -10%, #ffda6a 100%);
       background-size: 100%;
     }
     .emoji_angry .emoji_face {
       position: absolute;
       width: 100%;
       height: inherit;
       animation: angary-face 2s ease-in 0s infinite;
     }
     @keyframes angary-face {
       35%,60% {transform: translateX(0) translateY(10px) scale(0.9);}
       40% {transform: translateX(-5px) translateY(10px) scale(0.9);}
       45% {transform: translateX(5px) translateY(10px) scale(0.9);}
       50% {transform: translateX(-5px) translateY(10px) scale(0.9);}
       55% {transform: translateX(5px) translateY(10px) scale(0.9);}
     }
     .emoji_angry .emoji_eyebrows {
        position: absolute;
        left: calc(50% - 3px);
        top: 55px;
        width: 6px;
        height: 6px;
        border-radius: 50%;
        /*background: #fff;*/
        box-shadow: 
        -44px 5px 0 0 #000,
        -7px 16px 0 0 #000,
        7px 16px 0 0 #000,
        44px 5px 0 0 #000;
     }
     
     .emoji_angry .emoji_eyebrows:before, .emoji_angry .emoji_eyebrows:after {
        content: '';
        position: absolute;
        left: calc(50% - 25px);
        top: 0;
        width: 50px;
        height: 20px;
        border-radius: 50%;
        border: 6px solid #000;
        box-sizing: border-box;
        border-top-color: transparent ;
        border-right-color: transparent ;
        border-left-color: transparent ;
      
     }
     .emoji_angry .emoji_eyebrows:before {margin-left: -25px; transform: rotat
     .emoji_angry .emoji_eyebrows:after  {margin-left: 25px; transform: rotate
     
     .emoji_angry .emoji_eyes {
         position: absolute;
         left: calc(50% - 6px);
         top: 70px;
         width: 12px;
         height: 12px;
         border-radius: 50%;
         /*background: red;*/
         box-shadow: 25px 0 0 0 #000,-25px 0 0 0 #000;
       }
      
     .emoji_angry .emoji_mouth {
       position: absolute;
       left: calc(50% - 18px);
       bottom: 15px;
       width: 36px;
       height: 18px;
       border-radius: 50%;
       background: #000;
       animation: angry-mouth 2s ease-in 0s infinite;
     }
     @keyframes angry-mouth {
       35%,50% {height: 6px;
       bottom: 25px;}
     }
 </style>
```
