# 出门问问文本生成任务开源数据集

出门问问序列猴子文本生成微调数据集（以下简称序列猴子数据集）是服务于文本生成任务的高质量人工标注的问答数据集。本次开放 5,000 条问答对数据，主要服务于字词错误检测、字词错误纠正及文本润色等任务。

开放数据明细如下：

| 类型         | 语言 | 数量 | 来源 |
| ------------ | ---- | ---- | ---- |
| 字词错误检测 | 中文 | 5,000 | 自研 |
| 字词错误纠正 | 中文 | 5,000 | 自研 |
| 文本润色     | 中文 | 5,000 | 自研 |

## 数据格式简介

序列猴子数据集以 `JSONL` 类型文件提供。文件的每一行都是一个 `JSON` 格式的文本。其中，`JSON` 的格式为：

  ```json
  {"input": "<提问>", "target": "<回答>", "task": "<任务类别>"}
  ```

其中，`任务类别`说明如下：

| 任务类别            | 用途         |
| ------------------- | ------------ |
| `word_error_detect` | 字词错误检测 |
| `word_correct`      | 字词错误纠正 |
| `polish`            | 文本润色     |

## 数据下载

### 下载地址

序列猴子数据集的下载链接如下：
  - http://share.mobvoi.com:5000/sharing/HXB6QPLAi

也可通过扫描如下二维码来得到下载链接：<br>
  ![下载链接](../images/qr_code_ft_dl_addr.png)

### 完整性校验

序列猴子数据集的 `MD5` 摘要信息如下。在下载完成后，可通过使用对比该摘要信息来验证下载数据的完整性。
  - `0699c2130e2eacc7b3119489e608d739`

比如在Linux系统上，可使用如下命令来计算下载后数据的 `MD5` 摘要信息：

  ```shell
  md5sum <下载后保存的文件>
  ```

### 数据解压

为降低传输和存储带宽要求，序列猴子数据集以 `*.tar.bz2` 格式的压缩包形式来提供。请在下载完成之后进行解压，以得到最终的开源数据。

比如在Linux系统上，可使用如下命令来进行解压：

  ```shell
  tar xvfj <压缩包文件>
  ```