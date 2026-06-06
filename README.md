本项目已停止维护，推荐使用<a href="[超链接地址](https://github.com/wes-lin/Cloud189Checkin)" title="Cloud189Checkin">Cloud189Checkin</a>

# 天翼云盘自动签到脚本

## 简介
这是一个用于天翼云盘自动签到的Python脚本，支持多账户批量签到、抽奖，并通过PUSH PLUS推送结果。

## 功能特性
- ✅ 多账户批量签到
- ✅ 自动参与每日抽奖
- ✅ 支持PUSH PLUS推送结果
- ✅ 用户名脱敏显示
- ✅ 详细的执行日志
- ✅ 异常处理和错误报告

## 使用方法

### 1. 环境准备
确保系统已安装Python 3.x，并安装所需依赖包：
```bash
pip install requests rsa
```

### 2. 配置账户信息
设置环境变量`TIAN_YI_ACCOUNTS`，格式为：
```text
export TIAN_YI_ACCOUNTS="手机号1,密码1;手机号2,密码2"
```

### 3. 配置PUSH PLUS推送
获取PUSH PLUS的token并设置环境变量：
```text
export PUSH_PLUS_TOKEN="你的PUSH PLUS TOKEN"
```

## 青龙面板定时任务配置
如果使用青龙面板，可以添加定时任务：
- 脚本路径：`/ql/scripts/tianyi_cloud_signer.py`
- 定时规则：`0 9 * * *`（每天上午9点执行）

## 环境变量说明
| 变量名 | 说明 | 示例 |
|--------|------|------|
| `TIAN_YI_ACCOUNTS` | 天翼云盘账户信息 | `手机号1,密码1;手机号2,密码2` |
| `PUSH_PLUS_TOKEN` | PUSH PLUS推送token | `abc123...` |

## 推送效果
脚本执行完成后会通过PUSH PLUS发送以下信息：
- 执行时间
- 账户总数统计
- 成功/失败统计
- 每个账户的详细签到结果

## 注意事项
- 请妥善保管账户信息，建议使用环境变量方式配置
- 请遵守天翼云盘的相关服务条款
- 如遇验证码等安全验证，脚本可能无法正常工作

## 贡献
欢迎提交Issue和Pull Request来改进脚本功能。

## 许可证
MIT License
