# 高校分类结果订阅

本项目维护高校分类结果订阅的领域约定、角色边界与样例数据，供后端服务、接口和自动化验证统一使用。当前契约覆盖财政系统、招生系统、统计系统，并明确事件顺序、稳定游标、权限裁剪、安全重放等关键约束。

## 目录

- `domain/contract.json`：领域角色、状态、约束和样例。
- `src/domain_contract/`：契约读取与确定性校验。
- `tools/check_contract.py`：命令行摘要检查。
- `tests/`：契约完整性回归测试。

## 验证

测试命令：`python3 -m unittest discover -s tests -v`

编译命令：`python3 -m compileall -q src tools tests`

命令行检查：`python3 tools/check_contract.py domain/contract.json`
