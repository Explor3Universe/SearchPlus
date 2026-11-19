---
type: regex
pattern: 'claim wins|refutation wins|state owner|death query|cause query|\bduel\b|witness(es)? of the past|offscope|дуэл|владел\S* состояния|смерть-запрос|причина-запрос|свидетел\S* прошлого'
flags: i
match: not_contains
target: last_message
weight: 1
---

The final answer contains no internal methodology labels.
