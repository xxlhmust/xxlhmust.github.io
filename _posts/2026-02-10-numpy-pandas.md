
---
layout: post
title: "numpy与pandas"
date: 2026-02-10 14:00:00 +0800
categories: [python,数据处理库]
tags: [数组,表格数据]
author: xxlh
toc: true
comments: true
math: true
mermaid: false
pin: false
---

## 一、numpy类型
数据类型：数组

数据特性：<font color="red"><strong>所有元素的数据类型必须相同</strong></font>

常见操作：切片以及索引

## 二、pandas类型
数据类型：Series（一维） 和 DataFrame（二维）

数据特性：<font color="red"><strong>列内数据类型相同，列间数据类型可不同</strong></font>
## 三、NumPy与Pandas对比总结

| 特性 | NumPy | Pandas |
|------|-------|--------|
| 核心数据结构 | ndarray（n维数组） | Series（一维）、DataFrame（二维） |
| 数据类型 | 所有元素类型必须相同 | 列内相同，列间可不同 |
| 索引系统 | 数值索引（0,1,2,...） | 标签索引（可自定义行/列名） |
| 适用场景 | 数值计算、科学计算、矩阵运算 | 数据分析、表格处理、时间序列 |
| 缺失值处理 | 无原生支持（需用特殊值） | 原生支持NaN，丰富处理方法 |
| 数据对齐 | 按位置对齐 | 按标签自动对齐 |
| 性能特点 | 纯数值计算极快 | 结构化数据处理高效 |
| 文件IO | 支持简单格式（.npy, .txt） | 支持丰富格式（CSV、Excel、JSON、SQL等） |
| 学习曲线 | 相对平缓 | 功能丰富，需要时间掌握 |




