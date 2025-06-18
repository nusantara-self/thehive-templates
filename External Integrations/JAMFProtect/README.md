# JAMFProtect Integration

This folder contains practical resources for integrating JAMF Protect with TheHive.

---

## Practical Use-Cases
<!-- USE_CASES:START -->
* [Alert ingestion for JAMF Protect alerts](use-cases/alert-ingestion-jamf-protect.md)
<!-- USE_CASES:END -->

---
## Cortex Neurons

### Abstract

| Type | Name | Purpose |
|------|------|---------|
| Responder | [JAMFProtect_addHashtoPreventList](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/responders/JAMFProtect/JAMFProtect_addHashtoPreventList.json) | Add IOC to JAMF Protect - creates a custom prevent list for a hash |
| Responder | [JAMFProtect_removeHashfromPreventList](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/responders/JAMFProtect/JAMFProtect_removeHashfromPreventList.json) | Remove IOC on JAMF Protect - removes associated custom prevent list(s) containing the hash |
