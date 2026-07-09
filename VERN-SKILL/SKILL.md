---
name: vern-intranet-search
description: Search VERN (Vonage intranet at intranet.vonage.net) for HR policies, company holidays, announcements, org charts, travel policies, and other employee resources. Use this skill when a user asks about Vonage internal employee resources such as HR policies, remote work policies, travel reimbursement, company holidays, org charts, benefits, or any company-wide announcements hosted on the intranet.
---

# VERN Intranet Search

Search the Vonage intranet (VERN) for employee resources using Glean Search with `container_filter: "https://intranet.vonage.net"`.

## Search Patterns

Use targeted keywords with the VERN container filter:

| Category | Example Query Keywords |
|---|---|
| HR policies | `HR policy remote work`, `leave policy`, `code of conduct` |
| Holidays | `company holidays 2025`, `public holiday calendar` |
| Announcements | `company announcement`, `all-hands update` |
| Org charts | `org chart`, `organizational structure`, `reports to` |
| Travel | `travel policy`, `travel reimbursement`, `expense policy` |
| Benefits | `employee benefits`, `health insurance`, `401k` |

## Workflow

1. Run `glean_search` with the user's keywords and `container_filter: "https://intranet.vonage.net"`.
2. If results include relevant URLs, use `glean_document_reader` to fetch full content.
3. Present findings in a clear, organized format with direct links.

## Tips

- If no results are found, broaden the keywords and retry without the container filter as a fallback.
- For org chart questions, also try `employee_search` with the person's name.
