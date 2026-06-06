# xiyue
每日一言
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>每日一言</title>
    <style>
        * {margin:0;padding:0;box-sizing:border-box;}
        body {
            min-height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;
            background:#f5f7fa;color:#333;font-family:"Microsoft Yahei",sans-serif;padding:20px;
        }
        .box {max-width:600px;text-align:center;background:#fff;padding:40px 30px;border-radius:16px;box-shadow:0 4px 20px rgba(0,0,0,0.08);}
        h1 {font-size:22px;margin-bottom:30px;color:#555;}
        .sentence {font-size:18px;line-height:2;margin-bottom:25px;}
        .author {font-size:14px;color:#888;}
        .refresh {margin-top:30px;padding:10px 26px;border:none;background:#6c8cff;color:#fff;border-radius:30px;cursor:pointer;font-size:15px;}
        .refresh:hover {background:#5a7be6;}
    </style>
</head>
<body>
    <div class="box">
        <h1>每日一言</h1>
        <div class="sentence" id="text"></div>
        <div class="author" id="author"></div>
        <button class="refresh" onclick="getSentence()">换一句</button>
    </div>
<script>
const words = [
    {text:"心怀善意，所遇皆温柔。", author:"佚名"},
    {text:"慢慢来，好戏都在烟火里。", author:"佚名"},
    {text:"保持热爱，奔赴下一场山海。", author:"佚名"},
    {text:"愿日子清透，万事顺心。", author:"佚名"},
    {text:"生活平凡，但也闪闪发光。", author:"佚名"},
    {text:"心有暖阳，何惧人生荒凉。", author:"佚名"},
    {text:"追风赶月莫停留，平芜尽处是春山。", author:"古风"},
    {text:"前路浩浩荡荡，万事尽可期待。", author:"佚名"},
    {text:"把烦恼清空，才能装下快乐。", author:"佚名"},
    {text:"愿你遍历山河，仍觉人间值得。", author:"佚名"}
];
function getSentence(){
    let r = Math.floor(Math.random()*words.length);
    document.getElementById("text").innerText = words[r].text;
    document.getElementById("author").innerText = "—— "+words[r].author;
}
window.onload = getSentence;
</script>
</body>
</html>
