# G5/G9 产品修改记录

- 产品编号：$(@{number=86; product_id=JLZ-EDU-AG-017; chinese_name=财务经营分析; english_name=Finance Analytics Agent; repository_name=edu-finance-analytics-agent; repository_url=https://github.com/jinlize-tech/edu-finance-analytics-agent; product_type=Agent; category_code=07; category=07 财务运营中心; description=机构财务和经营数据分析。; target_users=System.Object[]; core_input=收入、成本、现金、应收、课包负债、班级与校区数据、统计口径; main_output=经营指标、趋势、结构分析、异常项、情景假设和管理建议; product_risk=口径不一致、用不完整数据预测或冒充审计; dedup_label=存在部分功能交叉; dedup_note=与校长经营OS LITE区分：限定财务经营分析，不提供完整经营操作系统；与财税OS相比不做税务合规。; development_status=Planned / 待研发; license=Apache-2.0; spec_version=1.0.0; workbuddy_status=PLANNED_FOR_WORKBUDDY}.product_id)
- 产品名称：财务经营分析
- 基线：EDUCATION_BASELINE_V1.0.0
- 基线提交：$BaselineCommit
- 原版本：1.0.0
- 新版本：1.0.1

## 本次修改

1. 强化产品专属执行流程、输入核对和输出验收规则。
2. 新增 scripts/validate_input.js，实际检查必填字段、冲突、未确认数据和敏感信息。
3. 新增正常、缺失、冲突、敏感信息和非法JSON场景输入。
4. 测试升级为 T1–T7 分层并保存逐项检查结果。
5. 安装包加入 Apache-2.0 LICENSE 和 THIRD_PARTY_NOTICES.md。
6. 安装包升级为 1.0.1，加入许可证、第三方声明和输入校验脚本，保留 1.0.0 ZIP。
7. 按本产品冻结规格补充专属处理规则、输入到成果的核对矩阵和去重边界。

## 产品专属增强

- 核心任务：机构财务和经营数据分析。
- 主要风险：口径不一致、用不完整数据预测或冒充审计
- 去重边界：与校长经营OS LITE区分：限定财务经营分析，不提供完整经营操作系统；与财税OS相比不做税务合规。

- 先统一会计期间、币种、含税口径、数据来源、分摊规则和舍入规则。
- 区分收入、已收款、应收、退款、固定成本、可变成本和现金流入。
- 每个数字保留来源、公式、单位与复核关系，不以测算替代会计或审计结论。
- 除零、负值、缺失值和规则冲突必须显式返回，不输出可执行付款或报税结论。

## 运行边界

- 本地模型行为：NOT_RUNTIME_VERIFIED
- WorkBuddy平台验证：WORKBUDDY_VALIDATION_NOT_IN_SCOPE
- 本轮不执行上传、安装、审核或正式发布。
