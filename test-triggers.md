# Rust Skills Trigger Test Checklist

> Run these queries in a project that has rust-skills installed, and verify the correct skill is triggered.

## How to Test

1. Go to a Rust project directory with rust-skills plugin installed
2. Run each query below with `claude -p "query"`
3. Check if the expected skill is triggered (shown in Claude Code status line)

---

## Ownership (m01-ownership)

| Query | Expected Skill |
|-------|----------------|
| `E0382 错误怎么解决` | m01-ownership |
| `value moved after use` | m01-ownership |
| `borrowed value does not live long enough` | m01-ownership |
| `怎么解决借用错误` | m01-ownership |
| `lifetime annotation` | m01-ownership |
| `E0597 lifetime too short` | m01-ownership |

## Resource (m02-resource)

| Query | Expected Skill |
|-------|----------------|
| `Arc 和 Rc 区别` | m02-resource |
| `Box vs Rc vs Arc` | m02-resource |
| `smart pointer 选择` | m02-resource |
| `shared ownership` | m02-resource |

## Mutability (m03-mutability)

| Query | Expected Skill |
|-------|----------------|
| `E0499 multiple mutable borrows` | m03-mutability |
| `E0502 borrow conflict` | m03-mutability |
| `E0596 cannot borrow as mutable` | m03-mutability |
| `Cell vs RefCell` | m03-mutability |
| `interior mutability` | m03-mutability |

## Zero-Cost (m04-zero-cost)

| Query | Expected Skill |
|-------|----------------|
| `E0277 trait bound not satisfied` | m04-zero-cost |
| `generic vs trait object` | m04-zero-cost |
| `monomorphization` | m04-zero-cost |
| `E0308 type mismatch` | m04-zero-cost |
| `E0282 type annotations needed` | m04-zero-cost |

## Error Handling (m06-error-handling)

| Query | Expected Skill |
|-------|----------------|
| `什么时候用 panic` | m06-error-handling |
| `Result vs Option` | m06-error-handling |
| `thiserror 怎么用` | m06-error-handling |
| `anyhow vs eyre` | m06-error-handling |
| `error propagation` | m06-error-handling |

## Concurrency (m07-concurrency)

| Query | Expected Skill |
|-------|----------------|
| `cannot be sent between threads` | m07-concurrency |
| `async await 怎么用` | m07-concurrency |
| `Send Sync trait` | m07-concurrency |
| `deadlock 怎么避免` | m07-concurrency |
| `如何在线程间共享数据` | m07-concurrency |

## Unsafe (unsafe-checker)

| Query | Expected Skill |
|-------|----------------|
| `unsafe 代码怎么写` | unsafe-checker |
| `FFI 绑定` | unsafe-checker |
| `SAFETY comment` | unsafe-checker |
| `raw pointer` | unsafe-checker |
| `how to call C functions` | unsafe-checker |

## Version/Crate (rust-learner)

| Query | Expected Skill |
|-------|----------------|
| `tokio 最新版本` | rust-learner |
| `Rust 1.85 有什么新特性` | rust-learner |
| `serde 文档` | rust-learner |
| `crate info` | rust-learner |

## Code Style (coding-guidelines)

| Query | Expected Skill |
|-------|----------------|
| `Rust 命名规范` | coding-guidelines |
| `clippy warning` | coding-guidelines |
| `rustfmt 配置` | coding-guidelines |
| `P.NAM.01` | coding-guidelines |

## Router (rust-router)

| Query | Expected Skill |
|-------|----------------|
| `分析这个问题的意图` | rust-router |
| `意图分析` | rust-router |
| `这是什么类型的 Rust 问题` | rust-router |

## Domains

| Query | Expected Skill |
|-------|----------------|
| `kubernetes operator in Rust` | domain-cloud-native |
| `decimal 精度计算` | domain-fintech |
| `机器学习 tensor` | domain-ml |
| `IoT sensor` | domain-iot |
| `axum web server` | domain-web |
| `clap CLI argument` | domain-cli |
| `no_std embedded` | domain-embedded |

---

## Quick Test Commands

```bash
# Test ownership
claude -p "E0382 错误怎么解决"

# Test mutability
claude -p "E0499 multiple mutable borrows"

# Test unsafe
claude -p "unsafe 代码怎么写"

# Test version
claude -p "tokio 最新版本"

# Test router
claude -p "分析这个问题的意图"
```

## Expected Behavior

When a skill triggers correctly, you should see:
1. The skill name in Claude Code's status line
2. Response content that matches the skill's expertise
3. References to patterns/rules from that skill

## Troubleshooting

If skills don't trigger:
1. Ensure rust-skills plugin is installed: `claude /plugins`
2. Check plugin path is correct
3. Verify SKILL.md files have `description:` field with keywords
4. Try more specific keywords from the skill description
