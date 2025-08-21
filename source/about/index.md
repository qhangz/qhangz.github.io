---
title: about
date: 2025-08-20 21:04:51
type: "about"
---
## 关于本站
<script>
    function secondToDate(second) {
        if (!second) return [0, 0, 0, 0, 0];
        var time = [0, 0, 0, 0, 0];
        if (second >= 365 * 24 * 3600) {
            time[0] = parseInt(second / (365 * 24 * 3600));
            second %= 365 * 24 * 3600;
        }
        if (second >= 24 * 3600) {
            time[1] = parseInt(second / (24 * 3600));
            second %= 24 * 3600;
        }
        if (second >= 3600) {
            time[2] = parseInt(second / 3600);
            second %= 3600;
        }
        if (second >= 60) {
            time[3] = parseInt(second / 60);
            second %= 60;
        }
        if (second > 0) {
            time[4] = second;
        }
        return time;
    }

    function setTime() {
        // 北京时间 2025-08-20 00:00:00
        var create_time = Math.floor(new Date(2025, 7, 20, 0, 0, 0).getTime() / 1000);
        // 当前时间秒数
        var timestamp = Math.floor(Date.now() / 1000);
        var currentTime = secondToDate(timestamp - create_time);
        var currentTimeHtml = currentTime[0] + ' 年 ' + currentTime[1] + ' 天 '
            + currentTime[2] + ' 时 ' + currentTime[3] + ' 分 ' + currentTime[4] + ' 秒';
        document.getElementById("htmer_time").innerHTML = currentTimeHtml;
    }
    setInterval(setTime, 1000);
</script>


- **本博客始建于 2025 年 08 月 20 日**
- <strong>距今已艰难运行了&nbsp;<span id="htmer_time"></span></strong>