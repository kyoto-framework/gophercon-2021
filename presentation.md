---
theme: default
class:
  - lead
  - invert
backgroundColor: #111
paginate: true
marp: true
---

![bg left:40% 80%](https://raw.githubusercontent.com/kyoto-framework/kyoto/master/docs/assets/kyoto.svg)

# **kyoto**

SSR-first Frontend Library

[https://kyoto.codes/](https://kyoto.codes/)

---

# Introduction

- Yurii Zinets
- Working at Akamai (Software Engineer L2)
- Working at BrokerOne on part time (Core Developer)

### Contacts

- Email: yurii.zinets@icloud.com
- Telegram: [@yuriizinets](https://t.me/yuriizinets)

---

# Why Go templates?

- Avoiding unnecessary complexity (tools, payloads, rendering steps)
- Full control over project setup
- Fewer problems in the runtime
- Simlier debugging

---

# What problems kyoto is trying to solve?

- Difficulties in following DRY with plain html templates approach
- Repeating DTO calls for each handler with reusable template parts
- Asynchronous DTO calls in handlers with goroutines is ... painful
- For dynamic things you still need to use JS and client-side DOM modification

---

# What features kyoto provides?

- Organizing code into configurable components structure
- Simple and straightforward page rendering lifecycle
- Asynchronous DTO without goroutine mess
- Built-in dynamics (like Hotwire or Laravel Livewire)

---

# Use cases

Not ready yet

---

# Future plans

- Advanced UI Kit
- Server Side State
- Running on the Edge Network

---

# Summary

- Presentation and notes are available on [https://github.com/kyoto-framework/kyoto](https://github.com/kyoto-framework/kyoto)