# 开源许可证商业风险对比

## 需要特别注意的许可证类型

### 1. 双许可证模式 (Dual License)
**典型代表：**
- MySQL (GPL + Commercial)
- Qt (LGPL + Commercial)
- MongoDB (SSPL + Commercial)

**特点：**
- ✅ 开源版本：免费，但有限制（如 GPL 要求开源）
- 💰 商业版本：需要付费购买商业许可证
- ⚠️ 风险：商业使用可能需要付费

**示例：**
```
如果你：
- 使用 MySQL GPL 版本
- 开发闭源商业产品
- 需要商业许可证（需付费）
```

### 2. AGPL (Affero General Public License)
**特点：**
- ✅ 可以修改和分发
- ❌ 如果提供网络服务，必须开源整个代码
- ⚠️ 某些变体可能要求保留"Powered by"

**商业风险：**
- SaaS 服务必须开源
- 不适合闭源商业产品

### 3. SSPL (Server Side Public License)
**典型代表：**
- MongoDB (2018年后)
- Elasticsearch (2021年后)

**特点：**
- ❌ 如果提供云服务，必须开源整个服务栈
- 💰 商业使用需要购买商业许可证
- ⚠️ 高风险：SaaS 服务必须开源或付费

### 4. 自定义许可证（要求保留品牌）
**典型特征：**
- 要求保留"Powered by XXX"
- 要求保留 Logo
- 禁止移除版权信息

**示例条款：**
```
"You may not remove or alter any copyright, trademark, 
or other proprietary notices, including 'Powered by XXX' 
text or logos, from the Software or any copies thereof."
```

### 5. 非商业许可证 (Non-Commercial License)
**典型代表：**
- Creative Commons Non-Commercial
- 某些"免费用于个人/教育用途"的许可证

**特点：**
- ✅ 个人/教育用途免费
- ❌ 商业用途需要付费或授权
- ⚠️ 风险：商业使用需要购买许可证

### 6. 共享源码许可证 (Shared Source License)
**典型代表：**
- Microsoft Shared Source Initiative (部分变体)

**特点：**
- ✅ 可以查看源代码
- ❌ 商业使用需要授权
- ⚠️ 风险：商业使用需要付费

### 7. BSL (Business Source License)
**典型代表：**
- MariaDB (部分组件)
- Sentry (部分组件)

**特点：**
- ✅ 源代码可见
- ❌ 商业使用需要授权（通常有时间限制）
- ⚠️ 风险：商业使用需要付费或等待许可证转换

## 许可证风险对比表

| 许可证类型 | UI标识可删除 | 商业使用免费 | 闭源销售 | 风险等级 |
|-----------|------------|------------|---------|---------|
| **MIT** | ✅ 可以 | ✅ 免费 | ✅ 可以 | 🟢 低 |
| **Apache 2.0** | ✅ 可以 | ✅ 免费 | ✅ 可以 | 🟢 低 |
| **BSD** | ✅ 可以 | ✅ 免费 | ✅ 可以 | 🟢 低 |
| **LGPL** | ✅ 可以 | ✅ 免费 | ⚠️ 需动态链接 | 🟡 中 |
| **GPL** | ✅ 可以 | ✅ 免费 | ❌ 必须开源 | 🟡 中 |
| **AGPL** | ⚠️ 看变体 | ✅ 免费 | ❌ SaaS需开源 | 🟡 中 |
| **SSPL** | ⚠️ 看变体 | ❌ 需付费 | ❌ 需付费 | 🔴 高 |
| **双许可证** | ✅ 可以 | ❌ 需付费 | ✅ 可以（付费后） | 🔴 高 |
| **BSL** | ✅ 可以 | ❌ 需付费 | ✅ 可以（付费后） | 🔴 高 |
| **自定义（要求品牌）** | ❌ 不能 | ⚠️ 看条款 | ⚠️ 看条款 | 🔴 高 |

## 需要特别警惕的许可证条款

### 1. 品牌保留条款
```license
"You must retain all copyright notices, trademarks, 
and 'Powered by XXX' attributions in the user interface."
```
**风险：** 不能删除 UI 上的品牌标识

### 2. 商业使用限制
```license
"This software is free for non-commercial use only. 
Commercial use requires a separate license agreement."
```
**风险：** 商业使用需要付费

### 3. SaaS 限制条款
```license
"If you offer this software as a service, you must 
make the entire service stack available under this license."
```
**风险：** SaaS 服务必须开源或付费

### 4. 分发限制
```license
"You may not distribute modified versions of this software 
without explicit written permission."
```
**风险：** 不能自由分发修改版本

## 如何识别风险许可证

### 检查清单：
1. ✅ 查看 LICENSE 文件
2. ✅ 搜索"commercial"、"paid"、"license fee"
3. ✅ 搜索"Powered by"、"attribution"、"brand"
4. ✅ 搜索"SaaS"、"service"、"cloud"
5. ✅ 检查是否有商业许可证选项
6. ✅ 查看项目官网是否有"Enterprise"版本

### 危险信号：
- 🚩 "Commercial license required"
- 🚩 "Enterprise edition"
- 🚩 "Contact us for commercial use"
- 🚩 "Powered by XXX must be retained"
- 🚩 "SaaS requires special license"

## 实际案例

### 案例 1：MongoDB SSPL
- **开源版本：** SSPL（要求 SaaS 开源）
- **商业版本：** 需要付费
- **风险：** 提供 MongoDB 作为服务必须开源或付费

### 案例 2：Elasticsearch
- **开源版本：** Elastic License（限制 SaaS）
- **商业版本：** 需要付费
- **风险：** 云服务提供商需要商业许可证

### 案例 3：某些 UI 框架
- **许可证：** 自定义许可证
- **要求：** 必须保留"Powered by XXX"
- **风险：** 不能删除品牌标识

## 建议

### 对于商业项目：
1. ✅ 优先选择：MIT、Apache 2.0、BSD
2. ⚠️ 谨慎使用：GPL、LGPL（需评估）
3. ❌ 避免使用：SSPL、BSL、双许可证（除非付费）
4. 🔍 仔细审查：自定义许可证

### 检查步骤：
1. 阅读完整的 LICENSE 文件
2. 检查是否有商业许可证选项
3. 搜索项目文档中的商业使用说明
4. 如有疑问，咨询法律顾问
