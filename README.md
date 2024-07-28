# QDAP-Chips

该仓库为[QDAP](https://github.com/ma6254/QDAP)的芯片器件库

## References

- <https://nodeca.github.io/js-yaml/>

## 芯片配置文件定义

### Vendor

| **Field** | **Type**                        | **Description** | **Required** |
| --------- | ------------------------------- | --------------- | ------------ |
| name      | string                          | 厂商名称        | Yes          |
| homepae   | string                          | 厂商网站主页    | No           |
| series    | [[]Series](README_zh.md#Series) | 系列            | Yes          |

### Series

| **Field**    | **Type**                            | **Description**       | **Required** |
| ------------ | ----------------------------------- | --------------------- | ------------ |
| name         | string                              | 系列名称              | Yes          |
| homepae      | string                              | 系列网站主页          | No           |
| pack_version | string                              | keil DFP pack version | No           |
| core         | string                              | 内核类型              | No           |
| ram_addr     | uint                                | 内存起始地址          | No           |
| flash_addr   | uint                                | 闪存起始地址          | No           |
| chips        | [[]ChipInfo](README_zh.md#ChipInfo) | 芯片                  | Yes          |

### ChipInfo

| **Field**  | **Type** | **Description**      | **Required** |
| ---------- | -------- | -------------------- | ------------ |
| name       | string   | 芯片名称             | Yes          |
| core       | string   | 内核类型             | No           |
| ram_size   | string   | 内存大小，例如"16KB" | No           |
| flash_size | string   | 闪存大小，例如"16KB" | No           |
| algo       | string   | 算法文件             | Yes          |
