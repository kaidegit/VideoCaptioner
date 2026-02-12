## 实现计划

修改 `main_window.py`，重写 `systemTitleBarRect` 方法，将 macOS 系统按钮（关闭/最小化/全屏）放到最左边，并调整标题栏布局。

### 具体修改

1. **重写 `systemTitleBarRect` 方法**：返回 `QRect(0, ...)` 让系统按钮从左边开始

2. **重写 `resizeEvent` 方法**：调整标题栏位置，为左边的系统按钮留出空间（约 75px），让返回按钮和标题显示在按钮右边

3. **调整 `FluentTitleBar` 布局**：在标题前添加左侧间距，为系统按钮预留空间

### 修改文件
- `/Volumes/aigo_1t/GitRepo/VideoCaptioner/app/view/main_window.py`