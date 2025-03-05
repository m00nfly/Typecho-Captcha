# Typecho-Captcha
Typecho专用验证码插件，支持中文、支持SAE

# 项目说明
本项目fork自 [Typecho-Captcha](https://github.com/KimiChen/Typecho-Captcha) 

因原作者已经 19 年没更新了，所以我基于该代码做了简单修改，兼容了 Typecho 1.2.1 版本和 PHP 8 环境。

# 功能更新

**2025.03.05 Update**
1. 修复在 PHP 8 下 securimage 无法生成验证码图片(破图)的 bug
2. 新增设置验证码位数的配置选项，可自定义生成验证码的字符数量（仅对非中文验证码生肖）
![image][2]
3. 新增了 ShortBaby.ttf 字体，对英文字母和数字提供更好的验证码效果

# 使用方法

1. [点击下载][1]最新的插件代码zip包
2. 解压缩后，将其中的 `Captcha` 目录上传到 Typecho 的 `usr/plugins/` 目录下
3. 在 Typecho 后台的插件管理界面，启用 Captcha 插件，并设置验证码相关参数
4. 在 Typecho 主题的评论页面 php 代码文件的合适位置插入如下代码，显示图片验证码
```php
<?php Captcha_Plugin::output(); ?>
```

# 测试
| Typecho 版本     | PHP 版本  | 结果 |
|----------------|---------|----|
| Typecho v1.2.1 | PHP 8.0 | ✅  | 


[1]:(https://github.com/m00nfly/Typecho-Captcha/zipball/master)
[2]:(data:image/jpeg;base64,/9j/4QDKRXhpZgAATU0AKgAAAAgABgESAAMAAAABAAEAAAEaAAUAAAABAAAAVgEbAAUAAAABAAAAXgEoAAMAAAABAAIAAAITAAMAAAABAAEAAIdpAAQAAAABAAAAZgAAAAAAAACQAAAAAQAAAJAAAAABAAeQAAAHAAAABDAyMjGRAQAHAAAABAECAwCgAAAHAAAABDAxMDCgAQADAAAAAQABAACgAgAEAAAAAQAAAkigAwAEAAAAAQAAAMakBgADAAAAAQAAAAAAAAAAAAD/2wCEABgYGBgYGCkYGCk6KSkpOk46Ojo6TmJOTk5OTmJ3YmJiYmJid3d3d3d3d3ePj4+Pj4+mpqampru7u7u7u7u7u7sBHR8fMCwwUSwsUcOEbYTDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw8PDw//dAAQAJf/AABEIAMYCSAMBIgACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/AOUooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooA/9DlKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAP/R5SiiigAooooAKt2tjc3jbYFyB1PQCixtWvLlYF4B6n0Ar0OGGOCMRRDaq9BQBy6eG5CP3kwB9lz/AIU//hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hGv+m//jn/ANej/hGv+m//AI5/9eupooA5b/hG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1qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA1f7a1P/nr/wCOr/hR/bWp/wDPX/x1f8KyqKANX+2tT/56/wDjq/4Uf21qf/PX/wAdX/CsqigDV/trU/8Anr/46v8AhR/bWp/89f8Ax1f8KyqKANX+2tT/AOev/jq/4Uf21qf/AD1/8dX/AArKooA0n1bUXGDMfwAH8hWezMx3Mck02igAooooAKKKKACiiigD/9LlKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAP/T5SiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD/2Q==)