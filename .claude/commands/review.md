# /review

## Intent
계획 대비 결과를 평가해 승인/반려를 판정한다.

## Input
- Required: task-id 또는 파일 범위

## Output
- `.sisyphus/evidence/<task-id>/review-report.md`

## Minimum Checklist
- [ ] scope gate
- [ ] quality gate
- [ ] verdict(APPROVED / CHANGES_REQUIRED / BLOCKED)
