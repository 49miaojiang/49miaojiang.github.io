# 49miaojiang.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>49miaojiang's Personal Website</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            overflow-x: hidden;
            background-color: #f5f5f5;
            transition: all 0.5s ease-in-out;
        }
        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            position: relative;
            text-align: center;
            color: white;
            opacity: 0;
            transform: translateY(20px);
        }
        .background-image {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://i.hd-r.icu/ab170a8752954a5019521c52f8443b67.png');
            background-size: cover;
            background-position: center;
            filter: blur(15px);
            z-index: -1;
        }
        .content {
            z-index: 1;
            max-width: 600px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
        }
        h1 {
            margin-bottom: 20px;
        }
        .social-icons a {
            margin: 0 10px;
            color: white;
            text-decoration: none;
            font-size: 2em;
            transition: color 0.3s ease-in-out;
        }
        .social-icons a:hover {
            color: #ffcc00;
        }
        .section {
            margin-top: 30px;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            margin: 10px 0;
        }
        .lang-switcher {
            position: fixed;
            bottom: 20px;
            right: 20px;
            cursor: pointer;
            color: white;
            font-size: 1em;
            transition: color 0.3s ease-in-out;
        }
        .lang-switcher:hover {
            color: #ddd;
        }
        @media (max-width: 600px) {
            .social-icons a {
                font-size: 1.5em;
            }
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            setTimeout(function() {
                document.querySelector('.container').style.opacity = '1';
                document.querySelector('.container').style.transform = 'translateY(0)';
            }, 500);

            const englishContent = {
                blogTitle: "Blog Articles",
                partnersTitle: "Partners",
                projectsTitle: "Projects",
                blogArticles: ["Blog Post 1", "Blog Post 2"],
                partners: [
                    { name: "别哭^", link: "https://v.kuaishou.com/Jl98Ygay" },
                    { name: "撞鬼秒倒", link: "https://v.kuaishou.com/J232AxZL" }
                ],
                projects: ["Project 1", "Project 2"]
            };
            
            const chineseContent = {
                blogTitle: "博客文章",
                partnersTitle: "合作伙伴",
                projectsTitle: "项目",
                blogArticles: ["文章1", "文章2"],
                partners: [
                    { name: "别哭^", link: "https://v.kuaishou.com/Jl98Ygay" },
                    { name: "撞鬼秒倒", link: "https://v.kuaishou.com/J232AxZL" }
                ],
                projects: ["项目1", "项目2"]
            };

            let currentLang = 'english';

            function updateContent(lang) {
                const content = lang === 'english' ? englishContent : chineseContent;
                document.getElementById('blog-title').textContent = content.blogTitle;
                document.getElementById('partners-title').textContent = content.partnersTitle;
                document.getElementById('projects-title').textContent = content.projectsTitle;

                document.querySelectorAll('#blog-list li').forEach((item, index) => {
                    item.innerHTML = `<a href="#" target="_blank"> $ {content.blogArticles[index]}</a>`;
                });

                document.querySelectorAll('#partners-list li').forEach((item, index) => {
                    const partner = content.partners[index];
                    item.innerHTML = `<a href=" $ {partner.link}" target="_blank"> $ {partner.name}</a>`;
                });

                document.querySelectorAll('#projects-list li').forEach((item, index) => {
                    item.innerHTML = `<a href="#" target="_blank"> $ {content.projects[index]}</a>`;
                });
            }

            document.querySelector('.lang-switcher').addEventListener('click', () => {
                currentLang = currentLang === 'english' ? 'chinese' : 'english';
                updateContent(currentLang);
            });

            updateContent(currentLang);
        });
    </script>
</head>
<body>
    <div class="container">
        <div class="background-image"></div>
        <div class="content">
            <h1>49miaojiang</h1>
            <div class="social-icons">
                <a href="https://b23.tv/bd6bvc8" target="_blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/bilibili.svg" alt="Bilibili" width="32" height="32"/></a>
                <a href="https://github.com/muxi-danran" target="_blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/github.svg" alt="GitHub" width="32" height="32"/></a>
                <a href="mailto:danranmuxi@outlook.com" target="_blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/outlook.svg" alt="Email" width="32" height="32"/></a>
            </div>
            <div class="section">
                <h2 id="blog-title">Blog Articles</h2>
                <ul id="blog-list">
                    <li><a href="#" target="_blank">Blog Post 1</a></li>
                    <li><a href="#" target="_blank">Blog Post 2</a></li>
                </ul>
            </div>
            <div class="section">
                <h2 id="partners-title">Partners</h2>
                <ul id="partners-list">
                    <li><a href="https://v.kuaishou.com/Jl98Ygay" target="_blank">别哭^</a></li>
                    <li><a href="https://v.kuaishou.com/J232AxZL" target="_blank">撞鬼秒倒</a></li>
                </ul>
            </div>
            <div class="section">
                <h2 id="projects-title">Projects</h2>
                <ul id="projects-list">
                    <li><a href="#" target="_blank">Project 1</a></li>
                    <li><a href="#" target="_blank">Project 2</a></li>
                </ul>
            </div>
        </div>
        <span class="lang-switcher">Toggle Language</span>
    </div>
</body>
</html>
