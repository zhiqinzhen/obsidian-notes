---
title: log 文件夹整理报告
date: 2026-09-14
tags:
  - 整理报告
  - 文件管理
aliases:
  - log整理报告
---

# log 文件夹整理报告

> [!success] 整理完成
> 原 `C:\Users\CM1071\Desktop\log\log` 的全部内容已按类别整理并迁移至 ==`D:\log`==,C 盘释放约 **1.3 GB** 空间,源目录已清空。

## 整理后的目录结构

```text
D:\log
├── 01-OA日志/        507M   15 项
├── 02-OA脚本/        216K   19 项
├── 03-OA文档/        5.1M   10 项
├── 04-个人简历/      1.3M    5 项
├── 05-课程资料/      1.1M    5 项
├── 06-个人文档/      332K    4 项
├── 07-媒体/          280M    2 项
├── 90-归档/          382M    2 项
├── tools/             78M   (ffmpeg,原样保留)
├── weaver-oa-dev/     42M   (git 仓库,原样保留)
├── .venv/            106M   (Python 虚拟环境,原样保留)
└── 新建文件夹/           0   (空目录,按需求保留)
```

## 各分类明细

### 01-OA日志(507M)
- 服务器日志目录:`10.0.10.65`、`10.0.10.68`、`65`、`68`、`查询特殊考勤日志`
- 散落日志:`ecology_20260720.log`(222M)、`jvm-app-0.log`、`emobile65/68.log`、`stderr/stdout.log`、`localhost_access_log.2026-08-20.txt`
- 压缩包:`0907日志.zip`、`日志.zip`、`日志新.zip`

### 02-OA脚本(19 个文件)
- 前端表单脚本:`att_change_form_custom.js`、`form_code_optimized.js`、`oa_*`系列、`付款流程提交校验.js`
- SQL 视图/清理:`v_hr_renyuan_info.sql`、`离职人员年假基数视图.sql`、`预算报表视图.sql`、`oa_location_cleanup.sql` 等
- 其他:`oa_check_role.jsp`、`nginx(1).conf`、`SynHrmResource`、`备份0831.txt`

### 03-OA文档(10 项)
- 流程文件:`入职办理流程.wewf`、`物料订单评审流程 (2).wewf`
- 说明文档:`oa_wflist_year_limit_说明.md`、`预算数据填报-数据表结构.md`、`weaver-oa-dev加密情况说明.md`
- 手册:`泛微移动平台飞书集成基础配置手册2021V1.0 (已自动恢复).docx`、`readme (4).docx`
- 商务:纯米科技尽调调查报告 + 电子签章合同
- 子目录:`路线B-明细导入优化`(原本已整理好,整体迁入)

### 04~07(个人与媒体)
- **04-个人简历**:3 版简历 PDF + `gen_resume_v2/v3.py` 生成脚本
- **05-课程资料**:少儿编程大纲、第四课/第五课 PDF + `gen_lesson5.py`、`gen_syllabus.py`
- **06-个人文档**:通讯录 2 份、梁文锋会议纪要、其他个人 PDF
- **07-媒体**:`视频/` 目录 + 微信图片

### 90-归档(382M)
- `lib.rar`(385M)、`ecology.zip`(14M)—— 体积大、访问频率低,归入归档

## 分类逻辑

- **01~03** 为泛微 OA 工作相关内容,按「日志 → 脚本 → 文档」的工作流顺序编号
- **04~06** 为个人内容,与工作完全分离
- **90** 开头表示冷数据归档,日常无需关注
- `tools`、`weaver-oa-dev`、`.venv` 属于功能性目录,保持原名不动

## 注意事项

> [!warning] .venv 虚拟环境
> 跨盘移动后,`.venv\Scripts\activate` 中的绝对路径已失效。如需继续使用,直接在 `D:\log` 下重建:`python -m venv .venv`,再重装依赖即可。

> [!tip] 后续维护建议
> - 新增 OA 日志直接放入 [[#01-OA日志(507M)|01-OA日志]],避免再次散落根目录
> - `90-归档` 中的 `lib.rar` 若确认无引用需求,可考虑删除,能再省 385M
> - 大日志文件(如 222M 的 ecology 日志)建议压缩后再留存

---
*由 Kimi Code 自动整理并生成,使用 kepano/obsidian-skills 的 obsidian-markdown 规范*
