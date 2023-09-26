<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JW</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 20px;
        }

        h1 {
            text-align: center;
            color: #333;
            opacity: 0;
            transform: translateY(-20px);
            transition: opacity 2s ease, transform 2s ease;
        }

        h2 {
            color: #555;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .page-intro {
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 20px;
            margin-bottom: 20px;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin-bottom: 20px;
            border: 1px solid #ddd;
            padding: 10px;
            border-radius: 5px;
        }

        a {
            text-decoration: none;
            color: #0077cc;
        }

        a:hover {
            text-decoration: underline;
        }

        p {
            color: #666;
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .search-button {
            background-color: #0077cc;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .return-button {
            background-color: #ccc;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
            color: #777;
        }

        .common-links {
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 20px;
            margin-bottom: 20px;
        }

    </style>
</head>
<body>
    <div class="container">
        <h1 id="welcome-heading">欢迎你！</h1>

        <div class="page-intro">
            <h2>我决不撇下你，决不离弃你。—— 来13:5</h2>
            <p></p>
        </div>

        <h2>可用的安装包：</h2>
        <input type="text" id="search" placeholder="搜索安装包">
        <button class="search-button" onclick="searchPackages()">搜索</button>
        <button class="return-button" onclick="returnToAllPackages()">返回</button>

        <ul id="package-list">
            <!-- 添加15个安装包链接位置 -->
            <li>
                <h3><a href="https://www.webex.com/content/dam/wbx/us/images/downloads/rebrand/mc.apk">Webex Meetings</a></h3>
                <p>描述：来自Cisco Systems, Inc
                    用于安排会议、开始会议等一系列操作
                    <br><b>请注意</b>:此安装包仅适用于Android 8.0及更高版本
                </p>
                <p>版本：43.9.0
                    <br>最近更新日期:2023年9月3日
                </p>
            </li>
            <li>
                <h3><a href="https://www.webex.com/content/dam/wbx/us/images/downloads/rebrand/uc.apk">Webex</a></h3>
                <p>描述：来自Cisco Systems, Inc
                    用于进行会议，当会议前的准备工作完成后将会自动跳转至此软件。需搭配Webex Meetings一起使用。
                    <br><b>请注意</b>:此安装包仅适用于Android 8.0及更高版本
                </p>
                <p>版本：43.9.0.113
                    <br>最近更新日期:2023年9月6日
                </p>
            </li>
            <li>
                <h3><a href="https://sweetcandy.tk/assets/archives/Android/ClashForAndroid-v2.5.12/cfa-2.5.12-premium-universal-release.apk">Clash For Android</a></h3>
                <p>描述：VPN软件
                    <br><b>请注意</b>:此安装包仅适用于Android 5.0及更高版本
                </p>
                <p>版本：2.5.12premium
                <br>最近更新日期:2022年11月16日
                </p>
                
            </li>
            <li>
                <h3><a href="链接到安装包3的URL">安装包3</a></h3>
                <p>描述：需添加请联系LSH</p>
                <p></p>
            </li>
        </ul>

        <div class="common-links">
            <h2>常用链接：</h2>
            <p>当通过浏览器进入Zoom会议： https://zoom.us/join</p>
            <p>当通过浏览器进入Webex会议： https://signin.webex.com/join</p>
            <p>链接3： 需添加请联系LSH</p>
        </div>
    </div>

    <div class="footer">
        <p>今天你读圣经了嘛？</p>
    </div>

    <script>
        window.onload = function () {
            var welcomeHeading = document.getElementById("welcome-heading");
            welcomeHeading.style.opacity = "1";
            welcomeHeading.style.transform = "translateY(0)";
        }

        function searchPackages() {
            var input = document.getElementById("search").value.toLowerCase();
            var packageList = document.getElementById("package-list");
            var packages = packageList.getElementsByTagName("li");

            for (var i = 0; i < packages.length; i++) {
                var packageName = packages[i].getElementsByTagName("h3")[0].textContent.toLowerCase();
                if (packageName.includes(input)) {
                    packages[i].style.display = "block";
                } else {
                    packages[i].style.display = "none";
                }
            }
        }

        function returnToAllPackages() {
            var packageList = document.getElementById("package-list");
            var packages = packageList.getElementsByTagName("li");

            for (var i = 0; i < packages.length; i++) {
                packages[i].style.display = "block";
            }
        }
    </script>
</body>
</html>
