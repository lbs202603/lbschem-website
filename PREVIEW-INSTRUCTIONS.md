# 🌐 宁波蓝宝石石油化工有限公司 - 官网预览

## 📥 方式 1：直接下载（最可靠）

### 步骤 1：复制以下代码
我已经把完整的网站代码放在下面了。

### 步骤 2：保存到本地
1. 在电脑上新建一个文本文件
2. 粘贴全部代码
3. 保存为 `index.html`
4. 双击打开即可预览

---

## 📄 完整网站代码

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="宁波蓝宝石石油化工有限公司 - 专业精细化学品供应商，代理陶氏、欧季亚、英力士等全球知名品牌，全国七大港口仓库，快速配送">
    <meta name="keywords" content="精细化学品，壬二酸，正戊酸，正戊醇，异戊醛，陶氏化学，欧季亚，蓝宝石化工，LBS Chemical">
    <meta name="author" content="宁波蓝宝石石油化工有限公司">
    <meta name="robots" content="index, follow">
    
    <title>宁波蓝宝石石油化工有限公司 | 专业精细化学品供应商</title>
    
    <style>
        :root {
            --primary-blue: #1e40af;
            --primary-light: #3b82f6;
            --accent-cyan: #06b6d4;
            --neutral-dark: #1f2937;
            --neutral-gray: #6b7280;
            --neutral-light: #f3f4f6;
            --white: #ffffff;
            --gradient-blue: linear-gradient(135deg, #1e40af 0%, #06b6d4 100%);
        }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans SC", sans-serif;
            line-height: 1.7;
            color: var(--neutral-dark);
            background: var(--white);
        }
        .container { max-width: 1280px; margin: 0 auto; padding: 0 24px; }
        .btn {
            display: inline-block;
            padding: 14px 32px;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
        }
        .btn-primary {
            background: var(--gradient-blue);
            color: var(--white);
            box-shadow: 0 4px 14px rgba(30, 64, 175, 0.3);
        }
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(30, 64, 175, 0.4);
        }
        .section { padding: 100px 0; }
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 16px;
            color: var(--neutral-dark);
        }
        .section-subtitle {
            text-align: center;
            color: var(--neutral-gray);
            font-size: 1.125rem;
            margin-bottom: 60px;
        }
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.08);
            z-index: 1000;
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 24px;
            max-width: 1280px;
            margin: 0 auto;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-blue);
            text-decoration: none;
        }
        .nav-links {
            display: flex;
            gap: 40px;
            list-style: none;
        }
        .nav-links a {
            text-decoration: none;
            color: var(--neutral-dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        .nav-links a:hover { color: var(--primary-blue); }
        .hero {
            padding: 200px 0 120px;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
        }
        .hero-content { text-align: center; max-width: 900px; margin: 0 auto; }
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 24px;
            background: var(--gradient-blue);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero p {
            font-size: 1.25rem;
            color: var(--neutral-gray);
            margin-bottom: 40px;
            line-height: 1.8;
        }
        .hero-stats {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 32px;
            margin-top: 80px;
        }
        .stat-item { text-align: center; }
        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            background: var(--gradient-blue);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .stat-label { color: var(--neutral-gray); margin-top: 8px; }
        .partners { background: var(--white); }
        .partners-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 40px;
            align-items: center;
            justify-items: center;
        }
        .partner-logo {
            height: 60px;
            opacity: 0.6;
            transition: opacity 0.3s;
            filter: grayscale(100%);
        }
        .partner-logo:hover { opacity: 1; filter: grayscale(0%); }
        .products { background: var(--neutral-light); }
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 32px;
        }
        .product-card {
            background: var(--white);
            border-radius: 16px;
            padding: 32px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(0,0,0,0.12);
        }
        .product-icon { font-size: 3rem; margin-bottom: 20px; }
        .product-card h3 { font-size: 1.5rem; margin-bottom: 12px; color: var(--neutral-dark); }
        .product-card p { color: var(--neutral-gray); line-height: 1.7; }
        .product-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
        .tag {
            background: #e0f2fe;
            color: var(--primary-blue);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.875rem;
            font-weight: 500;
        }
        .network { background: var(--white); }
        .network-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        .network-list { list-style: none; }
        .network-list li {
            padding: 16px 0;
            border-bottom: 1px solid var(--neutral-light);
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .network-list li::before {
            content: "✓";
            color: var(--primary-blue);
            font-weight: 700;
            font-size: 1.25rem;
        }
        .applications { background: var(--neutral-dark); color: var(--white); }
        .applications .section-title { color: var(--white); }
        .applications .section-subtitle { color: #9ca3af; }
        .applications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 24px;
        }
        .app-item {
            background: rgba(255,255,255,0.08);
            padding: 24px;
            border-radius: 12px;
            text-align: center;
            transition: background 0.3s;
        }
        .app-item:hover { background: rgba(255,255,255,0.12); }
        .app-icon { font-size: 2.5rem; margin-bottom: 12px; }
        .contact { background: var(--white); }
        .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; }
        .contact-info h3 { font-size: 1.5rem; margin-bottom: 24px; }
        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 16px;
            margin-bottom: 24px;
        }
        .contact-icon { font-size: 1.5rem; color: var(--primary-blue); }
        footer {
            background: var(--neutral-dark);
            color: #9ca3af;
            padding: 60px 0 30px;
        }
        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }
        .footer-section h4 { color: var(--white); margin-bottom: 20px; }
        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 12px; }
        .footer-links a {
            color: #9ca3af;
            text-decoration: none;
            transition: color 0.3s;
        }
        .footer-links a:hover { color: var(--white); }
        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .hero-stats { grid-template-columns: repeat(2, 1fr); }
            .network-content, .contact-grid, .footer-grid { grid-template-columns: 1fr; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="/" class="logo">LBS Chemical | 蓝宝石化工</a>
            <ul class="nav-links">
                <li><a href="#home">首页</a></li>
                <li><a href="#about">关于我们</a></li>
                <li><a href="#products">产品中心</a></li>
                <li><a href="#network">服务网络</a></li>
                <li><a href="#applications">应用领域</a></li>
                <li><a href="#contact">联系我们</a></li>
            </ul>
            <a href="#contact" class="btn btn-primary">立即咨询</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>连接全球优质化工资源<br>服务中国智造</h1>
                <p>宁波蓝宝石石油化工有限公司是一家专业从事精细化学品供应的服务商，代理陶氏、欧季亚、英力士等全球知名品牌，为全国客户提供高品质化工产品与技术服务</p>
                <div style="display: flex; gap: 16px; justify-content: center;">
                    <a href="#products" class="btn btn-primary">查看产品</a>
                    <a href="#contact" class="btn" style="background: var(--white); color: var(--primary-blue);">联系我们</a>
                </div>
            </div>
            <div class="hero-stats">
                <div class="stat-item">
                    <div class="stat-number">8+</div>
                    <div class="stat-label">全球合作品牌</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">7</div>
                    <div class="stat-label">港口仓库</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">10+</div>
                    <div class="stat-label">服务行业</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">24h</div>
                    <div class="stat-label">快速响应</div>
                </div>
            </div>
        </div>
    </section>

    <section class="section partners">
        <div class="container">
            <h2 class="section-title">全球合作伙伴</h2>
            <p class="section-subtitle">代理国际知名化工品牌，品质保证</p>
            <div class="partners-grid">
                <div class="partner-logo">美国陶氏 DOW</div>
                <div class="partner-logo">德国欧季亚 OXEA</div>
                <div class="partner-logo">德国英力士 INEOS</div>
                <div class="partner-logo">意大利 Matrica</div>
                <div class="partner-logo">韩国 SK</div>
                <div class="partner-logo">日本大赛璐 DAICEL</div>
                <div class="partner-logo">马来西亚 KLK</div>
                <div class="partner-logo">印尼春金 Musim Mas</div>
            </div>
        </div>
    </section>

    <section class="section products" id="products">
        <div class="container">
            <h2 class="section-title">核心产品系列</h2>
            <p class="section-subtitle">高品质精细化学品，满足多样化需求</p>
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-icon">🧪</div>
                    <h3>羧酸类产品</h3>
                    <p>正戊酸、正庚酸、正壬酸、辛酸、己酸等，广泛应用于香料、医药中间体</p>
                    <div class="product-tags">
                        <span class="tag">CAS 认证</span>
                        <span class="tag">欧洲标准</span>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-icon">💧</div>
                    <h3>醇类产品</h3>
                    <p>正戊醇、异戊醇、三甘醇等，用于溶剂、增塑剂、表面活性剂</p>
                    <div class="product-tags">
                        <span class="tag">99.99%</span>
                        <span class="tag">高纯度</span>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-icon">⚗️</div>
                    <h3>醛酮类产品</h3>
                    <p>异戊醛、环戊酮等，精细化工重要中间体</p>
                    <div class="product-tags">
                        <span class="tag">医药级</span>
                        <span class="tag">工业级</span>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-icon">🌿</div>
                    <h3>营养添加剂</h3>
                    <p>壬二酸等，用于化妆品、医药、食品添加剂</p>
                    <div class="product-tags">
                        <span class="tag">食品级</span>
                        <span class="tag">化妆品级</span>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-icon">🔬</div>
                    <h3>日化原料</h3>
                    <p>表面活性剂、乳化剂、增稠剂等日化专用化学品</p>
                    <div class="product-tags">
                        <span class="tag">天然来源</span>
                        <span class="tag">环保</span>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-icon">📦</div>
                    <h3>出口产品</h3>
                    <p>具备向国外输出优势产品的能力，服务全球客户</p>
                    <div class="product-tags">
                        <span class="tag">国际贸易</span>
                        <span class="tag">海关认证</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section network" id="network">
        <div class="container">
            <div class="network-content">
                <div>
                    <h2 class="section-title" style="text-align: left;">全国服务网络</h2>
                    <p style="color: var(--neutral-gray); margin-bottom: 32px;">七大港口仓库，就近发货，快速响应</p>
                    <ul class="network-list">
                        <li><strong>宁波</strong> - 总部基地，主要仓储中心</li>
                        <li><strong>上海</strong> - 华东配送中心</li>
                        <li><strong>南京</strong> - 江苏服务网点</li>
                        <li><strong>青岛</strong> - 华北仓储基地</li>
                        <li><strong>天津</strong> - 京津冀配送中心</li>
                        <li><strong>大连</strong> - 东北服务网点</li>
                        <li><strong>广州</strong> - 华南配送中心</li>
                    </ul>
                    <a href="#contact" class="btn btn-primary" style="margin-top: 32px;">查询库存</a>
                </div>
                <div style="background: linear-gradient(135deg, #e0f2fe 0%, #f0f9ff 100%); border-radius: 24px; padding: 40px; min-height: 400px; display: flex; align-items: center; justify-content: center;">
                    <div style="text-align: center;">
                        <div style="font-size: 4rem;">🗺️</div>
                        <p style="color: var(--neutral-gray); margin-top: 16px;">全国七大港口仓库<br>就近发货 · 快速配送</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section applications" id="applications">
        <div class="container">
            <h2 class="section-title">服务行业</h2>
            <p class="section-subtitle">为多行业提供专业化学品解决方案</p>
            <div class="applications-grid">
                <div class="app-item"><div class="app-icon">💊</div><div>医药</div></div>
                <div class="app-item"><div class="app-icon">🌾</div><div>农化</div></div>
                <div class="app-item"><div class="app-icon">🐾</div><div>动物营养</div></div>
                <div class="app-item"><div class="app-icon">🧴</div><div>日化</div></div>
                <div class="app-item"><div class="app-icon">📺</div><div>液晶中间体</div></div>
                <div class="app-item"><div class="app-icon">⚙️</div><div>润滑油</div></div>
                <div class="app-item"><div class="app-icon">🎨</div><div>涂料</div></div>
                <div class="app-item"><div class="app-icon">🍽️</div><div>食品添加剂</div></div>
                <div class="app-item"><div class="app-icon">🌸</div><div>香精香料</div></div>
                <div class="app-item"><div class="app-icon">💻</div><div>电子化学品</div></div>
            </div>
        </div>
    </section>

    <section class="section contact" id="contact">
        <div class="container">
            <h2 class="section-title">联系我们</h2>
            <p class="section-subtitle">期待与您合作共赢</p>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>宁波蓝宝石石油化工有限公司</h3>
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div><strong>地址</strong><p>浙江省宁波高新区新梅路 518 号奥创中心 A 幢 1604 室</p></div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📞</div>
                        <div><strong>电话</strong><p>0574-88332597</p></div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📠</div>
                        <div><strong>传真</strong><p>0574-88330798</p></div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📧</div>
                        <div><strong>邮箱</strong><p>lbs@lbschem.com</p></div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🛒</div>
                        <div><strong>阿里巴巴商城</strong><p><a href="https://shop4098xo3096590.1688.com" target="_blank">https://shop4098xo3096590.1688.com</a></p></div>
                    </div>
                </div>
                <div style="background: var(--neutral-light); border-radius: 24px; padding: 40px;">
                    <h3 style="margin-bottom: 24px;">快速咨询</h3>
                    <form style="display: grid; gap: 20px;">
                        <input type="text" placeholder="您的姓名" style="width: 100%; padding: 14px; border: 1px solid #d1d5db; border-radius: 8px; font-size: 1rem;">
                        <input type="email" placeholder="邮箱地址" style="width: 100%; padding: 14px; border: 1px solid #d1d5db; border-radius: 8px; font-size: 1rem;">
                        <input type="tel" placeholder="联系电话" style="width: 100%; padding: 14px; border: 1px solid #d1d5db; border-radius: 8px; font-size: 1rem;">
                        <textarea placeholder="咨询内容" rows="4" style="width: 100%; padding: 14px; border: 1px solid #d1d5db; border-radius: 8px; font-size: 1rem; resize: vertical;"></textarea>
                        <button type="submit" class="btn btn-primary">提交咨询</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-section">
                    <h4>宁波蓝宝石石油化工有限公司</h4>
                    <p style="line-height: 1.8;">专业精细化学品供应服务商，连接全球优质化工资源，服务中国智造</p>
                </div>
                <div class="footer-section">
                    <h4>快速链接</h4>
                    <ul class="footer-links">
                        <li><a href="#home">首页</a></li>
                        <li><a href="#about">关于我们</a></li>
                        <li><a href="#products">产品中心</a></li>
                        <li><a href="#contact">联系我们</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>产品中心</h4>
                    <ul class="footer-links">
                        <li><a href="#products">羧酸类</a></li>
                        <li><a href="#products">醇类</a></li>
                        <li><a href="#products">醛酮类</a></li>
                        <li><a href="#products">营养添加剂</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>合作伙伴</h4>
                    <ul class="footer-links">
                        <li>美国陶氏</li>
                        <li>德国欧季亚</li>
                        <li>德国英力士</li>
                        <li>韩国 SK</li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>版权所有 © 2016-2026 宁波蓝宝石石油化工有限公司 | 浙 ICP 备 16012839 号</p>
                <p style="margin-top: 8px; font-size: 0.875rem;">网络支持：中国化工网 | 全球化工网 | 生意宝</p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

## 📥 方式 2：从服务器下载

**文件位置：**
```
/home/admin/.openclaw/workspace/lbschem-website/index.html
```

你可以用 FTP 工具或 SCP 命令下载到本地：
```bash
scp admin@your-server:/home/admin/.openclaw/workspace/lbschem-website/index.html ~/Desktop/
```

---

## 🎨 网站内容概览

1. **导航栏** - Logo + 菜单 + 咨询按钮
2. **Hero 区** - 大标题 + 数据统计
3. **合作伙伴** - 8 家国际品牌
4. **产品中心** - 6 大产品系列
5. **服务网络** - 7 大港口仓库
6. **应用领域** - 10 个服务行业
7. **联系我们** - 完整信息 + 表单
8. **页脚** - 版权信息

---

**最简单的方式：复制上面的代码 → 保存为 index.html → 双击打开！**

需要我帮你做任何调整吗？😊
