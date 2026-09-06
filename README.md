
---

## 不过，上面这个版本我建议再做一处重要调整

**不要现在手工填写全部 `[Paper](LINK)`。**

因为你的 Table 4 里已经有 **62 篇 surveyed studies**，而且正文第 31–33 页已经明确统计了：

- ECG：34/62
- EEG：19/62
- PPG：7/62
- wearable：8/62
- disease classification：28.2%
- signal understanding：37.2%
- health monitoring：17.9%
- signal synthesis：6.4%

这些是你 review 的核心 corpus。:contentReference[oaicite:3]{index=3}

所以真正好的 GitHub 应该是**把 Table 4 的 62 篇研究系统地迁移过来**，而不是只放十几篇代表性文章。

---

# 我建议 Paper Collection 最终用这种格式

例如：

### Medical Disease Diagnosis

```markdown
| Method | Year | Modality | LLM / Architecture | Role of LLM | Prompt | Dataset | Task | Paper | Code |
|---|---:|---|---|---|---|---|---|---|---|
| GEM | 2025 | ECG | GPT-4o + ECG-CoCa + SFT-LLaVA | Text decoder / multimodal model | Clinical-guided | MIMIC-IV-ECG, PULSE, ECG-Bench | Grounded ECG understanding | [Paper](...) | [Code](...) |
