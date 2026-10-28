# 清风阅读 · 公版书库 (Brisa Reader Public Catalog)

这是一个全平台通用、纯静态、符合标准 OPDS 1.2 规范的多语种公开版权书库。

- **标准 OPDS 1.2 根目录**：`https://books.uni3k.com/opds/root.xml`
- **本地检索索引**：`https://books.uni3k.com/index.json`
- **支持语言**：繁體中文 (zh-Hant)、English (en)、日本語 (ja)
- **提供格式**：标准 EPUB 完整下载包、逐章 XHTML 极速在线阅读页面

---

## 包含书目概览 (首批 60 部经典名著)

### 1. 中文古典典籍与名著（31 部）
- **经部**：《論語》、《孟子》、《周易》、《尚書》、《詩經》、《禮記》、《春秋左氏傳》、《孝經》
- **子部**：《莊子》、《道德經》、《孫子兵法》、《荀子》、《韓非子》、《墨子》、《管子》、《列子》
- **史部**：《史記》、《戰國策》、《山海經》
- **集部**：《楚辭》、《文心雕龍》、《唐詩三百首》、《宋詞三百首》
- **章回小说与散文**：《三國演義》、《水滸傳》、《西遊記》、《紅樓夢》、《封神演義》、《東周列國志》、《世說新語》、《浮生六記》

### 2. 英文世界传世名著（22 部）
- **福尔摩斯探案系列**：*A Study in Scarlet*, *The Sign of the Four*, *The Adventures of Sherlock Holmes*, *The Memoirs of Sherlock Holmes*, *The Hound of the Baskervilles*
- **科幻与探险传奇**：*Twenty Thousand Leagues Under the Sea*, *Around the World in Eighty Days*, *Treasure Island*, *Robinson Crusoe*, *The Time Machine*
- **经典文学小说**：*Pride and Prejudice*, *Sense and Sensibility*, *Jane Eyre*, *A Tale of Two Cities*, *The Great Gatsby*, *The Adventures of Tom Sawyer*, *The Call of the Wild*
- **童话诗歌与哲学**：*Alice's Adventures in Wonderland*, *The Happy Prince and Other Tales*, *The Raven*, *Walden*, *The Art of War (Lionel Giles)*

### 3. 日文名家杰作（7 部）
- **夏目漱石**：《こころ》（心）、《吾輩は猫である》（我是猫）、《坊っちゃん》（少爷）
- **芥川龙之介**：《羅生門》（罗生门）、《蜘蛛の糸》（蜘蛛之丝）、《鼻》（鼻）
- **森鸥外**：《舞姫》（舞姬）

---

## 目录结构

```text
.
├── index.json                  # 全局轻量检索索引（书名、别名、作者、朝代、字数/词数统计）
├── opds/                       # OPDS 1.2 导航目录
│   ├── root.xml                # 根导航（全部书籍 / 按语言 / 按分类）
│   ├── all.xml                 # 全部书籍获取条目
│   ├── lang/                   # 分语言浏览 (zh-Hant.xml, en.xml, ja.xml)
│   └── category/               # 分分类浏览 (jing.xml, fiction.xml, philosophy.xml 等)
└── books/                      # 每部图书的实体资源
    └── <book-id>/
        ├── <book-id>.epub      # 完整 EPUB 电子书下载
        ├── manifest.json       # 章节元数据、SHA-256 校验与权利声明
        ├── style.css           # 针对语种排版的自适应样式
        └── chapters/           # 逐章 XHTML 文件，供移动端/桌面端极速在线流式阅读
```

---

## 版权与许可声明 (Copyright & License)

- **正文文本**：全部属于公有领域（Public Domain）。中文古籍为古代传世作品；外文书籍均在作者去世 70 年以上或 1929 年以前发表。
- **排版与整理**：版式与校勘依据维基文库（Wikisource）志愿者社区整理成果，遵循 **CC BY-SA 4.0** 许可协议。
