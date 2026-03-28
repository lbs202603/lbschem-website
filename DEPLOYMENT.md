# LBS Chemical 官网 - 部署与 SEO 优化指南

## 📦 一、部署步骤

### 1. 准备工作

#### 1.1 域名与 SSL
```bash
# 确认域名解析
# A 记录：www.lbschem.com → 服务器 IP
# A 记录：lbschem.com → 服务器 IP

# 申请 SSL 证书（免费 Let's Encrypt）
sudo certbot --nginx -d lbschem.com -d www.lbschem.com
```

#### 1.2 服务器环境
```bash
# 推荐配置
- Nginx 1.20+
- Ubuntu 20.04+ / CentOS 8+
- 2GB+ RAM
- SSD 存储
```

### 2. 上传网站文件

```bash
# 方法 A：SCP 上传
scp -r lbschem-website/* user@your-server:/var/www/lbschem.com/

# 方法 B：FTP 上传
# 使用 FileZilla 等工具上传到 /var/www/lbschem.com/

# 方法 C：Git 部署
cd /var/www/lbschem.com
git clone https://github.com/your-repo/lbschem-website.git .
```

### 3. Nginx 配置

创建配置文件 `/etc/nginx/sites-available/lbschem.com`：

```nginx
server {
    listen 80;
    server_name lbschem.com www.lbschem.com;
    
    # 强制 HTTPS
    return 301 https://$server_name$request_uri;
}

server {
    listen 443 ssl http2;
    server_name lbschem.com www.lbschem.com;
    
    root /var/www/lbschem.com;
    index index.html;
    
    # SSL 证书
    ssl_certificate /etc/letsencrypt/live/lbschem.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/lbschem.com/privkey.pem;
    
    # SSL 优化
    ssl_protocols TLSv1.2 TLSv1.3;
    ssl_prefer_server_ciphers on;
    ssl_ciphers ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512;
    
    # Gzip 压缩
    gzip on;
    gzip_vary on;
    gzip_min_length 1024;
    gzip_types text/plain text/css text/xml text/javascript application/javascript application/json application/xml+rss;
    
    # 静态资源缓存
    location ~* \.(css|js|png|jpg|jpeg|gif|ico|svg|woff|woff2|ttf|eot)$ {
        expires 1y;
        add_header Cache-Control "public, immutable";
    }
    
    # HTML 不缓存（便于更新）
    location ~* \.html$ {
        expires 1h;
        add_header Cache-Control "public, must-revalidate";
    }
    
    # 安全头
    add_header X-Frame-Options "SAMEORIGIN" always;
    add_header X-Content-Type-Options "nosniff" always;
    add_header X-XSS-Protection "1; mode=block" always;
    
    location / {
        try_files $uri $uri/ =404;
    }
}
```

启用配置：
```bash
sudo ln -s /etc/nginx/sites-available/lbschem.com /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
```

---

## 🔍 二、SEO 优化清单

### 1. 技术 SEO ✅

- [x] 语义化 HTML5 标签
- [x] Meta 标签完整（title, description, keywords）
- [x] JSON-LD 结构化数据
- [x] 移动端响应式
- [x] HTTPS 加密
- [x] 快速加载（内联 CSS）
- [ ] XML 站点地图（sitemap.xml）
- [ ] robots.txt 配置
- [ ] 规范化标签（canonical）

### 2. 页面 SEO ✅

- [x] 唯一且描述性的标题（每页不同）
- [x] Meta 描述（150-160 字符）
- [x] 关键词自然分布
- [x] 标题层级（H1 → H2 → H3）
- [x] 图片 Alt 文本
- [x] 内部链接结构
- [ ] 面包屑导航
- [ ] 分页标签（rel=next/prev）

### 3. 内容 SEO ✅

- [x] 核心关键词覆盖
- [x] 长尾关键词（产品名 + CAS 号）
- [x] 行业术语（医药中间体、日化原料等）
- [x] 品牌词（LBS Chemical、蓝宝石化工）
- [ ] 博客/新闻内容（定期更新）
- [ ] 常见问题（FAQ）
- [ ] 客户案例

### 4. 本地 SEO ✅

- [x] 公司名称、地址、电话（NAP）一致
- [x] Google My Business / 百度地图标注
- [x] 结构化数据（Organization）
- [ ] 本地关键词（宁波化工、浙江精细化学品）

---

## 📝 三、提交搜索引擎

### 1. 百度搜索资源平台

1. 访问：https://ziyuan.baidu.com/
2. 注册账号
3. 添加网站（www.lbschem.com）
4. 验证所有权（HTML 文件验证）
5. 提交 sitemap.xml
6. 使用"主动推送"功能

```xml
<!-- sitemap.xml 示例 -->
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://www.lbschem.com/</loc>
        <lastmod>2026-03-28</lastmod>
        <changefreq>weekly</changefreq>
        <priority>1.0</priority>
    </url>
    <url>
        <loc>https://www.lbschem.com/product-pentanoic-acid.html</loc>
        <lastmod>2026-03-28</lastmod>
        <changefreq>monthly</changefreq>
        <priority>0.8</priority>
    </url>
</urlset>
```

### 2. Google Search Console

1. 访问：https://search.google.com/search-console
2. 添加网站
3. 验证所有权
4. 提交 sitemap.xml
5. 监控索引状态

### 3. Bing Webmaster Tools

1. 访问：https://www.bing.com/webmasters
2. 导入 Google Search Console 数据
3. 提交 sitemap.xml

---

## 📊 四、性能优化

### 1. 图片优化

```bash
# 转换 WebP 格式
convert logo.png -quality 85 logo.webp

# 压缩图片
tinypng logo.png
```

### 2. 启用 CDN

推荐服务商：
- 阿里云 CDN（国内）
- 腾讯云 CDN（国内）
- Cloudflare（全球）

### 3. 性能监控

```bash
# Lighthouse 测试
npm install -g lighthouse
lighthouse https://www.lbschem.com --view

# PageSpeed Insights
# https://pagespeed.web.dev/
```

---

## 📈 五、数据分析

### 1. 百度统计

```html
<!-- 添加到 <head> -->
<script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?YOUR_TOKEN";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>
```

### 2. Google Analytics

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

---

## 🔧 六、日常维护

### 每周
- [ ] 检查网站可访问性
- [ ] 查看统计数据
- [ ] 回复咨询表单

### 每月
- [ ] 更新新闻动态
- [ ] 检查 SEO 排名
- [ ] 备份网站数据
- [ ] 更新产品信息

### 每季度
- [ ] 全面 SEO 审计
- [ ] 性能优化
- [ ] 内容更新
- [ ] 安全检查

---

## 📞 七、技术支持

### 常见问题

**Q: 网站打不开？**
```bash
# 检查 Nginx 状态
sudo systemctl status nginx

# 查看错误日志
sudo tail -f /var/log/nginx/error.log
```

**Q: SSL 证书过期？**
```bash
# 续期
sudo certbot renew
```

**Q: 如何更新网站？**
```bash
# 直接替换文件
scp index.html user@server:/var/www/lbschem.com/

# 或 Git 拉取
cd /var/www/lbschem.com
git pull origin main
```

---

## ✅ 八、上线前检查清单

- [ ] 域名解析正确
- [ ] SSL 证书有效
- [ ] Nginx 配置正确
- [ ] 网站可正常访问
- [ ] 移动端显示正常
- [ ] 所有链接有效
- [ ] 联系表单可用
- [ ] 404 页面配置
- [ ] 提交搜索引擎
- [ ] 安装统计代码
- [ ] 备份网站数据

---

*最后更新：2026 年 3 月 28 日*
