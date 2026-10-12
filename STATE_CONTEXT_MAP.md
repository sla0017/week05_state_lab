# 상태 계약 및 흐름도

- **이벤트→상태→UI 흐름:** 리스트 타일 탭(완료 버튼) → `_toggleDone(index)` 실행 → `_todos[index].isDone` 값 반전 → `_remainingCount` 재계산 → 상단 AppBar의 숫자 및 리스트 아이콘/텍스트 취소선 업데이트
- **원본 상태:** `List<TodoItem> _todos` 내부의 `isDone` 여부
- **계산값:** `_remainingCount` (완료되지 않은 항목의 수)
- **상태 소유자:** `_TodoListScreenState`