用户当前使用小米 xiaomi 提供商 (mimo-v2.5-pro)。kuaipao.ai 自定义端点已配置可用，支持模型：claude-fable-5, claude-haiku-4-5, claude-opus-4-6, claude-opus-4-7, claude-opus-4-8, claude-sonnet-4-6。切换提供商时需同时设置 provider 和 model.default。
§
用户使用 kuaipao.ai (https://kuaipao.ai/v1) 作为自定义 Claude 模型供应商，支持的模型名: claude-opus-4-8, claude-opus-4-7, claude-opus-4-6, claude-sonnet-4-6, claude-haiku-4-5, claude-fable-5。配置方式: model.provider=custom + model.base_url=https://kuaipao.ai/v1 + model.default=<模型名>。该 token 曾出现额度/失效导致的 401 错误。
§
用户的小米模型配置: model.provider=xiaomi, model.default=mimo-v2.5-pro (注意必须用完整名 mimo-v2.5-pro，简写 mimo/MiMo 会报 400 不支持)。端点 https://token-plan-cn.xiaomimimo.com/v1。
§
小米模型图片识别：mimo-v2.5-pro 不支持图片识别/vision，需要图片分析时切换到 mimo-v2.5（非pro版本）。
§
环境：libredwg已通过brew安装，提供dwg2dxf工具。可转换AC1032(AutoCAD 2018)格式DWG文件为DXF，然后用ezdxf读取。天正(TCH)自定义实体会被跳过但不影响核心数据提取。春湾中学电气DWG文件(电施_t8.dwg)包含完整电气系统图和平面图，已成功提取2ALG/2ALE/AL2-4/防雷系统信息。
§
macOS上weasyprint不可用（缺少gobject/pango共享库）。生成中文PDF用pymupdf + china-s内置字体，无需额外依赖。
§
Markdown转Word流程：①用matplotlib生成流程图PNG（中文字体用PingFang SC/Heiti SC）②用python-docx生成Word，含表格、层级标题、加粗、列表③流程图以doc.add_picture(width=Inches(5.5))嵌入并居中。脚本路径/tmp/gen_docx.py可复用。注意Python字符串中中文引号用\u201c\u201d转义避免语法错误。
§
pptxgenjs全局安装后Node找不到模块。修复：在项目目录本地安装 `cd /tmp/ppt_project && npm init -y && npm install pptxgenjs`，然后从该目录运行 `node create_ppt.js`。
§
中文文件名含括号（如"项目管理(5).docx"）时，bash内联python -c会解析失败。解决：写成.py脚本文件再执行，不要用inline -c。读取格式：.doc用textutil转txt，.docx用python-docx，.xlsx用openpyxl。