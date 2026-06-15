用户当前使用小米 xiaomi 提供商 (mimo-v2.5-pro)。kuaipao.ai 自定义端点已配置可用，支持模型：claude-fable-5, claude-haiku-4-5, claude-opus-4-6, claude-opus-4-7, claude-opus-4-8, claude-sonnet-4-6。切换提供商时需同时设置 provider 和 model.default。
§
用户使用 kuaipao.ai (https://kuaipao.ai/v1) 作为自定义 Claude 模型供应商，支持的模型名: claude-opus-4-8, claude-opus-4-7, claude-opus-4-6, claude-sonnet-4-6, claude-haiku-4-5, claude-fable-5。配置方式: model.provider=custom + model.base_url=https://kuaipao.ai/v1 + model.default=<模型名>。该 token 曾出现额度/失效导致的 401 错误。
§
用户的小米模型配置: model.provider=xiaomi, model.default=mimo-v2.5-pro (注意必须用完整名 mimo-v2.5-pro，简写 mimo/MiMo 会报 400 不支持)。端点 https://token-plan-cn.xiaomimimo.com/v1。
§
小米模型图片识别：mimo-v2.5-pro 不支持图片识别/vision，需要图片分析时切换到 mimo-v2.5（非pro版本）。
§
环境：libredwg已通过brew安装，提供dwg2dxf工具。可转换AC1032(AutoCAD 2018)格式DWG文件为DXF，然后用ezdxf读取。天正(TCH)自定义实体会被跳过但不影响核心数据提取。春湾中学电气DWG文件(电施_t8.dwg)包含完整电气系统图和平面图，已成功提取2ALG/2ALE/AL2-4/防雷系统信息。