# little-surprise
little-surprise

<style>
/* 整体容器：夜空渐变背景 */
.qixi-container {
  position: relative;
  max-width: 650px;
  margin: 60px auto;
  padding: 50px 40px;
  border-radius: 24px;
  background: linear-gradient(135deg, #0c1445 0%, #1a237e 40%, #283593 100%);
  color: #f0f0ff;
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
  overflow: hidden;
  box-shadow: 0 15px 50px rgba(26, 35, 126, 0.4);
}

/* 漫天星空闪烁效果 */
.qixi-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(2px 2px at 30px 40px, #ffffff, transparent),
    radial-gradient(2px 2px at 80px 90px, #fffacd, transparent),
    radial-gradient(1.5px 1.5px at 120px 60px, #ffffff, transparent),
    radial-gradient(2px 2px at 180px 110px, #ffb6c1, transparent),
    radial-gradient(1px 1px at 220px 30px, #ffffff, transparent),
    radial-gradient(2px 2px at 280px 140px, #ffd700, transparent),
    radial-gradient(1.5px 1.5px at 350px 80px, #ffffff, transparent),
    radial-gradient(2px 2px at 420px 50px, #ffc0cb, transparent),
    radial-gradient(1px 1px at 480px 130px, #ffffff, transparent),
    radial-gradient(2px 2px at 550px 90px, #fffacd, transparent),
    radial-gradient(1.5px 1.5px at 590px 40px, #ffffff, transparent),
    radial-gradient(2px 2px at 100px 180px, #ffd700, transparent),
    radial-gradient(1px 1px at 300px 200px, #ffffff, transparent),
    radial-gradient(2px 2px at 500px 190px, #ffb6c1, transparent);
  background-size: 650px 250px;
  animation: twinkle 3.5s ease-in-out infinite alternate;
  pointer-events: none;
  z-index: 1;
}

/* 星星闪烁动画 */
@keyframes twinkle {
  0% { opacity: 0.4; }
  100% { opacity: 1; }
}

/* 浮动爱心装饰 */
.float-heart {
  position: absolute;
  font-size: 22px;
  color: #ff6b9d;
  animation: heartFloat 5s ease-in-out infinite;
  pointer-events: none;
  z-index: 2;
  opacity: 0.8;
}
.float-heart:nth-of-type(1) { top: 12%; left: 8%; animation-delay: 0s; }
.float-heart:nth-of-type(2) { top: 18%; right: 12%; animation-delay: 1.2s; font-size: 18px; color: #ff8fab; }
.float-heart:nth-of-type(3) { bottom: 35%; left: 6%; animation-delay: 2.5s; font-size: 20px; color: #ffc8dd; }
.float-heart:nth-of-type(4) { bottom: 20%; right: 8%; animation-delay: 1.8s; font-size: 24px; color: #ff6b9d; }

/* 爱心上下浮动动画 */
@keyframes heartFloat {
  0%, 100% {
    transform: translateY(0) rotate(-5deg);
  }
  50% {
    transform: translateY(-25px) rotate(8deg);
  }
}

/* 文案逐行淡入上浮 */
.qixi-content {
  position: relative;
  z-index: 3;
  font-size: 19px;
  line-height: 2.1;
  letter-spacing: 0.5px;
}
.qixi-content p {
  margin: 16px 0;
  opacity: 0;
  animation: fadeInUp 1s ease forwards;
}
.qixi-content p:nth-child(1) { animation-delay: 0.4s; }
.qixi-content p:nth-child(2) { animation-delay: 1.2s; }
.qixi-content p:nth-child(3) { animation-delay: 2s; }

/* 文字淡入动画 */
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(25px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* 重点词句发光效果 */
.glow-text {
  color: #ffe066;
  font-weight: 500;
  animation: textGlow 2.2s ease-in-out infinite alternate;
}

/* 文字呼吸发光动画 */
@keyframes textGlow {
  0% {
    text-shadow: 0 0 4px #ffe066, 0 0 8px rgba(255, 224, 102, 0.5);
  }
  100% {
    text-shadow: 0 0 10px #ffe066, 0 0 20px #ff8fab, 0 0 30px rgba(255, 107, 157, 0.4);
  }
}
</style>

<div class="qixi-container">
  <span class="float-heart">♡</span>
  <span class="float-heart">♥</span>
  <span class="float-heart">♡</span>
  <span class="float-heart">♥</span>

  <div class="qixi-content">
    <p>今年七夕，银河依旧横贯夜空，而我最幸运的事，是不用等鹊桥相会，<span class="glow-text">一转头就能看见你</span>。</p>
    <p>从前觉得七夕只是传说里的浪漫，直到遇见你才懂，真正的心动，是<span class="glow-text">把每一个平凡日子都过成佳期</span>。</p>
    <p>往后的<span class="glow-text">岁岁年年</span>，想和你一起看遍人间烟火，也守好彼此的温柔。</p>
  </div>
</div>