# dashang
打赏排行榜源码 [独家]
此打赏源码是二开别人的，想找原版的某度一下打赏源码应该就会有的，把付款页面和排行榜分离出来，又做了些细节上的改动，然后又花了66块钱叫人适配Wordpress侧边栏，哎 我真是钱多老是喜欢折腾网站，之前有几个管我要都没给，现在直接分享。 应该是可以适应其他网站的侧边栏的 不懂的话把侧边栏代码丢给AI，他能帮你搞定，其他也不知道说什么，不善于表达，看下方演示地址吧 
# 免费下载：链接：https://pan.xunlei.com/s/VOcCQef03_fRxDRaM4OGHRR8A1?pwd=n3ed# 复制这段内容后打开「手机迅雷 App」即可获取。无需下载在线查看，视频原画享倍速播放
# 我用夸克网盘分享了「dx_2025-10-20_21-25-59_mysql_data_kYD6c.sql.zip」，点击链接即可保存。打开「夸克APP」，无需下载在线播放视频，畅享原画5倍速，支持电视投屏。
链接：https://pan.quark.cn/s/d7dbe63675f0
<img width="1440" height="632" alt="image" src="https://github.com/user-attachments/assets/392a66c8-6b71-4ad2-bda5-f14e375071cf" />
<img width="1440" height="692" alt="image" src="https://github.com/user-attachments/assets/05a7f99c-ded8-4316-a527-31e82635942d" />

<img width="877" height="781" alt="image" src="https://github.com/user-attachments/assets/78a8f825-0bd4-485a-a7d4-58a7d0ba897d" />



<style>
/* 顶部添加空格：保持之前微调后的高度 */
.top-spacing {
height: 8px;
}

.ranking-container {
margin-top: 15px; /* 保持容器顶部间距不变 */
}

@media (min-width: 768px) {
.ranking-container {
margin-top: 0;
}
}

.ranking-container .ranking-number {
font-weight: bold;
font-size: 0.9rem; /* 减小字体 */
}

.ranking-container .ranking-list {
max-height: 500px;
overflow-y: auto;
scrollbar-width: none;
scrollbar-color: #0d6efd #f8f9fa;
}

.ranking-container .ranking-list::-webkit-scrollbar {
width: 4px;
}

.ranking-container .ranking-list::-webkit-scrollbar-track {
background: #f8f9fa;
}

.ranking-container .ranking-list::-webkit-scrollbar-thumb {
background-color: #0d6efd;
border-radius: 3px;
}

.ranking-container .ranking-item {
padding: 6px 0;
border-bottom: 1px solid rgba(0, 0, 0, 0.05);
transition: background-color 0.3s;
}

.ranking-container .ranking-item:last-child {
border-bottom: none;
}

.ranking-container .ranking-item:hover {
background-color: rgba(13, 110, 253, 0.03);
}

.ranking-container .ranking-avatar {
width: 40px;
height: 40px;
border-radius: 50%;
object-fit: cover;
}

.ranking-container .ranking-info {
flex: 1;
min-width: 0;
margin: 0 10px;
}

.ranking-container .ranking-amount {
font-weight: 600;
color: #0d6efd;
white-space: nowrap;
font-size: 0.95rem; /* 保持原有大小 */
}

@media (max-width: 576px) {
.ranking-container .ranking-item {
padding: 10px 8px;
}

.ranking-container .ranking-avatar {
width: 35px;
height: 35px;
}

.ranking-container .ranking-info {
margin: 0 8px;
}

.ranking-container .ranking-amount {
font-size: 0.9rem; /* 保持原有大小 */
}

.ranking-container .ranking-number {
font-size: 0.8rem; /* 减小字体 */
min-width: 24px;
}

/* 手机端样式调整 */
.ranking-container {
margin: 0;
}

.ranking-container .card {
border-radius: 0;
margin: 0;
}

.ranking-container .card-body {
padding: 15px;
}

.ranking-container .ranking-list {
max-height: none;
overflow-y: visible;
}

.ranking-container .ranking-list::-webkit-scrollbar {
display: none;
}
}

.ranking-container .card {
border: none;
border-radius: 20px;
margin-bottom: 0px;
background: white;
box-shadow: unset;
overflow: hidden;
}

.ranking-container .card-body {
padding: 12px 16px; /* 保持卡片内边距不变 */
}

/* 顶部文字样式：仅减小标题底部间距，让下方展示更靠近顶部 */
.ranking-container .card-title {
color: #2c3e50;
font-weight: 700;
font-size: 1.1rem;
margin-bottom: 5px; /* 从12px减至8px，仅靠近一点点 */
display: flex;
justify-content: center;
align-items: center;
gap: 13px;
padding: 5px 0;
}

/* 按钮样式：保持之前调整好的尺寸 */
.card-title .donate,
.card-title .more {
font-size: 12px;
transform: none;
padding: 3px 8px;
color: #F1404A !important;
border: 0.5px solid #F1404A;
border-radius: 5px;
display: inline-block;
transition: all 0.2s ease;
}

.card-title .donate:hover,
.card-title .more:hover {
background-color: rgba(241, 64, 74, 0.1);
}

/* 标题图标颜色加深 */
.card-title .text-warning {
color: #fd7e14 !important;
}

@media (max-width: 768px) {
.ranking-container {
margin: 0;
}

.ranking-container .card {
border-radius: 0;
margin: 0;
}

.ranking-container .card-body {
padding: 15px;
}

.ranking-container .ranking-list {
margin-bottom: 0;
}

.ranking-container .ranking-item {
padding-bottom: 8px;
}

/* 移动端顶部文字适配：同步减小标题底部间距 */
.ranking-container .card-title {
gap: 9px;
font-size: 1rem;
margin-bottom: 8px;
}
}

.ranking-container .ranking-list::-webkit-scrollbar {
width: 4px;
}

.io-black-mode .ranking-container .card {
background: #2c2e2f;
}

.io-black-mode .ranking-container .card-title {
color: #fff;
}

/* 深色模式按钮样式：保持不变 */
.io-black-mode .card-title .donate,
.io-black-mode .card-title .more {
font-size: 12px;
padding: 3px 8px;
color: #ff6b6b !important;
border: 0.5px solid #ff6b6b;
border-radius: 5px;
}

.io-black-mode .card-title .donate:hover,
.io-black-mode .card-title .more:hover {
background-color: rgba(255, 107, 107, 0.1);
}

/* 新增渐变动画样式 */
@keyframes rainbow-gradient {
0% {
background-position: 100% 50%;
}
100% {
background-position: -100% 50%;
}
}

.gradient-text {
background: linear-gradient(to left, red, orange, yellow, green, blue, indigo, violet);
background-size: 200% 100%;
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
animation: rainbow-gradient 3s linear infinite;
}

/* 调整其他字体大小 */
.ranking-info .fw-bold {
font-size: 0.9rem; /* 减小用户名字体 */
white-space: nowrap; /* 强制在一行显示 */
overflow: hidden; /* 隐藏溢出内容 */
text-overflow: ellipsis; /* 溢出部分显示省略号 */
}

.ranking-info small {
font-size: 0.78rem; /* 减小网址字体 */
white-space: nowrap; /* 强制在一行显示 */
overflow: hidden; /* 隐藏溢出内容 */
text-overflow: ellipsis; /* 溢出部分显示省略号 */
display: block; /* 确保占据一行 */
}
</style>

<div class="top-spacing"></div> <!-- 顶部空格区域保持不变 -->

<div>
<div class="ranking-container">
<!-- 排行榜前的固定文字 -->
<div class="card">
<div class="card-body">
<h5 class="card-title text-center mb-4">
<a href="https://789bh.com/12345-2" class="more gradient-text" target="_blank">查看更多</a>
<span><i class="fas fa-crown text-warning me-2"></i>捐赠排行榜</span>
<a href="https://789bh.com/ds/" class="donate gradient-text" target="_blank">支持一下</a>
</h5>
<div id="rankingList" class="ranking-list">
<!-- 排行榜将通过 JavaScript 动态加载 -->
</div>
</div>
</div>
<!-- 排行榜后的固定文字 -->
</div>
</div>

<script src="https://lf26-cdn-tos.bytecdntp.com/cdn/expire-1-M/jquery/3.6.0/jquery.min.js"></script>
<script src="https://lf9-cdn-tos.bytecdntp.com/cdn/expire-1-M/bootstrap/5.1.3/js/bootstrap.bundle.min.js"></script>
<script>
$(document).ready(function () {
/* 加载排行榜数据 */
function loadRanking() {
$.get('https://789bh.com/ds/api/get_ranking.php', function (response) {
if (response.code === 0) {
const { rankings, statistics } = response.data;

/* 更新排行榜 */
const rankingHtml = rankings.map((rank, index) => {
let url = rank.website;
let urlText = url? `感谢${url}` : '暂无网址信息';
return `
<div class="ranking-item d-flex align-items-center">
<img src="${rank.avatar}" class="ranking-avatar" alt="头像"
style="border: 2px solid ${index < 3? '#ffd700' : '#e9ecef'}">
<div class="ranking-info">
<div class="text-truncate fw-bold">${rank.qq}</div>
<small class="text-muted"><a href="${url || '#'}" target="_blank" class="gradient-text">${urlText}</a></small>
</div>
<div class="ranking-amount">
¥${rank.total_amount.toFixed(2)}
</div>
</div>
`;
}).join('');

$('#rankingList').html(rankingHtml);
}
});
}

/* 初始加载排行榜 */
loadRanking();
/* 每60秒刷新一次排行榜 */
setInterval(loadRanking, 60000);
});
</script>



对页面排版或美化不满意可以找AI,遇事不觉找AI
