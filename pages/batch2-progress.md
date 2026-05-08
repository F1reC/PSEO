# PSEO 第二批 50 页生成进度

> 开始时间：2026-05-07
> 目标：再生成 50 个模板页面，更新 index.html

---

## 总体进度

| # | 步骤 | 状态 | 备注 |
|---|------|------|------|
| 1 | 选定 50 个 app | ✅ 完成 | 16 个 marketplace 未用 + 34 个爬取 |
| 2 | 验证 50 个图片 URL | ✅ 完成 | 全部 HTTP 200 |
| 3 | 读取模板结构 (CSS+HTML) | ✅ 完成 | 基于 ecommerce-store.html |
| 4 | 收集所有 app 元数据 | ✅ 完成 | 名称/描述/图片/分类 |
| 5 | 写 Python 生成脚本 | ❌ 未开始 | 下一步 |
| 6 | 生成 50 个 HTML 文件 | ❌ | |
| 7 | 更新 pages.md | ❌ | 添加 #53-#102 |
| 8 | 更新 pages-tracking.md | ❌ | |
| 9 | 更新 gen_index_v3.py | ❌ | 添加 50 条新记录 |
| 10 | 重新生成 index.html | ❌ | |

---

## 已选定的 50 个 App

### A. Marketplace 未用 (16 个)

| # | App ID | 名称 | 分类 | 图片 URL |
|---|--------|------|------|----------|
| 1 | app-6xtuimqa9wqp | EcoStyle Nordic | Education | `https://miaoda-edit-image.s3cdn.medo.dev/6xtuimqa9wqp/IMG-6xuu6vyhj9j4.png` |
| 2 | app-9281q1vjh1c1 | PAIR | Education | `https://miaoda-edit-image.s3cdn.medo.dev/9281q1vjh1c1/IMG-928dqdjbxo8w.jpg` |
| 3 | app-7xtdx45my6m9 | Sistema de Correcao de Provas | Education | `https://miaoda-edit-image.s3cdn.medo.dev/7xtdx45my6m9/IMG-7xxrnn3svaps.png` |
| 4 | app-8ffi5ay5u4n5 | OM'S JARVIS | Productivity | `https://miaoda-edit-image.s3cdn.medo.dev/8ffi5ay5u4n5/IMG-8fkfnw5v5iio.png` |
| 5 | app-8rkazpf5umtd | Mutabakat Sistemi | Productivity | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8rkazpf5umtd/app-8rkazpf5umtd_1767782789989_e029.png` |
| 6 | app-8edo7k9ws2kh | Record Management App | Productivity | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8edo7k9ws2kh/app-8edo7k9ws2kh_1766391500152_a512.png` |
| 7 | app-8gtt17gdrkzl | Premium 3D E-Commerce Mobile App | E-commerce | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8gtt17gdrkzl/app-8gtt17gdrkzl_1766630641514_11cd.png` |
| 8 | app-7z8w46v33im9 | Delivered In Area | E-commerce | `https://miaoda-edit-image.s3cdn.medo.dev/7z8w46v33im9/IMG-7zaubxchua68.png` |
| 9 | app-9j7j21d1sf0h | Personal Schedule Dashboard | Website | `https://miaoda-edit-image.s3cdn.medo.dev/9j7j21d1sf0h/IMG-9j95t6hslf5s.png` |
| 10 | app-9y0vsccu1og1 | Developer CV | Website | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9y0vsccu1og1/app-9y0vsccu1og1_1774872288992_ebe3.png` |
| 11 | app-96zmwyspfksh | Affiliate Program Landing Page | Website | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-96zmwyspfksh/app-96zmwyspfksh_1778065283861_0732.png` |
| 12 | app-8yvk8vptzdhd | Hari Krupa Bakery | Marketing | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8yvk8vptzdhd/app-8yvk8vptzdhd_1768550555093_d800.png` |
| 13 | app-925f8glcvs3m | MOUS | Marketing | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-925f8glcvs3m/app-925f8glcvs3m_1768901395642_1e43.png` |
| 14 | app-7ku6mhekukn6 | Conquest World | Games | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7ku6mhekukn6/app-7ku6mhekukn6_1773030396753_63fa.png` |
| 15 | app-7rdfmfcymn0h | Dominoes | Games | `https://miaoda-edit-image.s3cdn.medo.dev/7rdfmfcymn0h/IMG-7rdx8vqqh3wg.png` |
| 16 | app-8klu0wgmoa9t | Browin's School Days | Games | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8klu0wgmoa9t/app-8klu0wgmoa9t_1768183745295_8f6a.png` |

### B. 爬取的 App (34 个)

| # | App ID | 名称 | 图片 URL |
|---|--------|------|----------|
| 17 | app-7h1s8had6zup | StockHub Pro | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7h1s8had6zup/app-7h1s8had6zup_1764334187030_2a7f.png` |
| 18 | app-7dihte45ynep | Himalayan Voyager | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7dihte45ynep/app-7dihte45ynep_1762446801371_d256.png` |
| 19 | app-6xqqt1yhj9j5 | IndigiLearn Canada | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-6xqqt1yhj9j5/app-6xqqt1yhj9j5_1760775534758_571f.png` |
| 20 | app-6s62524vrb41 | Virtual Aquarium | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-6s62524vrb41/app-6s62524vrb41_1760174029114_91b1.png` |
| 21 | app-80r4tjsb3g8x | Fitness Tracker | `https://miaoda-edit-image.s3cdn.medo.dev/80r4tjsb3g8x/IMG-81lhos29bbi8.png` |
| 22 | app-7pey5m0o0qv5 | Food Delivery App | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7pey5m0o0qv5/app-7pey5m0o0qv5_1763712582388_a8a3.png` |
| 23 | app-88v11906rg1t | California Coffee House | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-88v11906rg1t/app-88v11906rg1t_1765783299594_4322.png` |
| 24 | app-99dqtz340cn5 | TheHandStandShop | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-99dqtz340cn5/app-99dqtz340cn5_1769667127163_11cb.png` |
| 25 | app-9qocfl6bgxdu | ReMind Me | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9qocfl6bgxdu/app-9qocfl6bgxdu_1771507814807_88ff.png` |
| 26 | app-ae410yygr30h | SalaryTrack | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-ae410yygr30h/app-ae410yygr30h_1774002130110_1e92.png` |
| 27 | app-a8hqyi3k4wzl | POS System | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-a8hqyi3k4wzl/app-a8hqyi3k4wzl_1773403689759_7718.png` |
| 28 | app-9mek38ytqhhd | 3D Pixel Maze Adventure | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9mek38ytqhhd/app-9mek38ytqhhd_1771052984892_2e06.png` |
| 29 | app-9jjka57t9fk1 | Brainrot Bot Shooter | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9jjka57t9fk1/app-9jjka57t9fk1_1771336841632_3633.png` |
| 30 | app-anq6462z2qyq | TypeMaster Pro | `https://miaoda-edit-image.s3cdn.medo.dev/anq6462z2qyq/IMG-anrxeuvy00e8.png` |
| 31 | app-ar28ns9jyznm | Live AQI Checker | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-ar28ns9jyznm/app-ar28ns9jyznm_1775379132710_41a1.png` |
| 32 | app-ah8riq0m1mv5 | SafeHer | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-ah8riq0m1mv5/app-ah8riq0m1mv5_1774336598902_ead7.png` |
| 33 | app-9x8qmeswmk8x | Online Voting System | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9x8qmeswmk8x/app-9x8qmeswmk8x_1772263095196_f02a.png` |
| 34 | app-aoudmzgntmv5 | DigiStore | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-aoudmzgntmv5/app-aoudmzgntmv5_1775150683540_6d03.png` |
| 35 | app-af3qw2qdea69 | MediDirect | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-af3qw2qdea69/app-af3qw2qdea69_1775054777971_601f.png` |
| 36 | app-a9mjoojpn5dt | SAGA.AI | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-a9mjoojpn5dt/app-a9mjoojpn5dt_1773524363257_6f1d.png` |
| 37 | app-8jlo57vkyl8h | MeetConnect | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8jlo57vkyl8h/app-8jlo57vkyl8h_1766924602299_b819.png` |
| 38 | app-9sxjvpqa6hhd | Productivity Leveling | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-9sxjvpqa6hhd/app-9sxjvpqa6hhd_1771748783120_afc8.png` |
| 39 | app-ato2pyigj08x | Electronic World | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-ato2pyigj08x/app-ato2pyigj08x_1775657445936_2f03.png` |
| 40 | app-8niwe9tbxzb5 | Flowgram | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-8niwe9tbxzb5/app-8niwe9tbxzb5_1767342064808_55de.png` |
| 41 | app-7yj37jhn5qf5 | Jarvis AI Assistant | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7yj37jhn5qf5/app-7yj37jhn5qf5_1764682242499_63f6.png` |
| 42 | app-85r7u9607uv5 | Personal Cash Flow Manager | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-85r7u9607uv5/app-85r7u9607uv5_1767044349393_02d5.png` |
| 43 | app-89mq2nordmv5 | Hospito | `https://miaoda-edit-image.s3cdn.medo.dev/89mq2nordmv5/IMG-89o7dt2zf4lc.png` |
| 44 | app-a9htejevm329 | Home Finder | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-a9htejevm329/app-a9htejevm329_1773511022814_2939.png` |
| 45 | app-7oo7lxgbhl35 | Steampunk Pier Cannon | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-7oo7lxgbhl35/app-7oo7lxgbhl35_1763633201620_3b24.png` |
| 46 | app-aad8103b1zb5 | Third Place Finder | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-aad8103b1zb5/app-aad8103b1zb5_1773602666818_f637.png` |
| 47 | app-83u0v1tglb7l | Rubycrypt | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-83u0v1tglb7l/app-83u0v1tglb7l_1765250678237_caf5.png` |
| 48 | app-a5jhq6kscr29 | Automotive Hero Section | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-a5jhq6kscr29/app-a5jhq6kscr29_1773088997924_bd24.png` |
| 49 | app-abixep6cdl35 | Professional Portfolio | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-abixep6cdl35/app-abixep6cdl35_1773727598122_5e37.png` |
| 50 | app-753nr4sxrapt | HEXVERSE | `https://miaoda-screenshot-img.s3cdn.medo.dev/preview_screen/app-753nr4sxrapt/app-753nr4sxrapt_1761551875910_4bea.png` |

---

## 爬取数据文件

| 文件 | 路径 | 说明 |
|------|------|------|
| 全部 app ID | `/tmp/all_medo_apps.txt` | 15,455 个 app ID，来自 sitemap |
| 爬取结果 | `/tmp/scraped_apps.txt` | 428 条，格式 `appid\|\|\|title\|\|\|desc\|\|\|img` |
| 爬取脚本 | `/tmp/scrape_app.sh` | 单个 app 子域名 OG 元数据爬取 |

---

## 模板结构参考

基于 `ecommerce-store.html`（535 行），结构：

```
JSON-LD (@graph: SoftwareApplication + BreadcrumbList + FAQPage)
<style> 完整 CSS (lines 70-268，所有页面复用)
<div class="medo-tpl">
  FEATURES (mt-split 左右分栏)
  PERFECT FOR (mt-pf-grid 6 张受众卡片)
  HOW IT WORKS (mt-steps 3 步骤 + mt-prompt 推荐框)
  CTA BOX (深色渐变背景)
  RELATED TEMPLATES (mt-related 3 张跨类别卡片)
  BUILT WITH MEDO (mt-showcase 3 张 showcase 卡片)
  FAQ (4 个 details/summary)
  FOOTER
</div>
```

---

## 下一步

1. 为 50 个 app 分配页面主题（文件名、H1 标题、分类、features、audience 等）
2. 写 Python 生成脚本 → 输出 50 个 HTML 文件到 `/Users/f1rec/GitHub/PSEO_ghost/PSEO/pages/`
3. 更新 `pages.md` 添加 #53-#102
4. 更新 `pages-tracking.md` 添加新页面
5. 更新 `/tmp/gen_index_v3.py` 添加 50 条记录
6. 重新生成 `index.html`
