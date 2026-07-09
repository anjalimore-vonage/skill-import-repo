# VERN Intranet Search Skill

## Overview
This skill helps users search VERN (Vonage intranet at intranet.vonage.net) for HR policies, holidays, company announcements, org charts, travel policies, and other employee resources.

## Usage
Use this skill when you need to find information in the Vonage intranet (VERN) regarding employee resources.

## Implementation

### Available Tools
The skill leverages Glean Search with specific filters for VERN content.

### Search Functionality
The skill provides targeted search capabilities for common VERN categories:
- HR policies
- Company holidays
- Announcements
- Organizational charts
- Travel policies
- General employee resources

### Search Approach
When invoked, the skill will:
1. Search VERN using appropriate keywords for the requested category
2. Filter results to only show relevant employee resources
3. Present findings in a clear, organized format

## Example Usage
"Find the latest HR policy on remote work" 
"Show me upcoming company holidays for 2026"
"What are the current travel reimbursement policies?"
"Who reported to John Smith in the organization chart?"

## Implementation Details

The skill uses the following search patterns:
- `query: "HR policy remote work" + container_filter: "https://intranet.vonage.net"`
- `query: "company holiday" + container_filter: "https://intranet.vonage.net"`