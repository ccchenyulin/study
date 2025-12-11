
# yazi配置说明文档https://github.com/jaywcjlove/reference/blob/main/docs/yazi.md
# 参考配置：https://github.com/theniceboy/.config/blob/master/yazi/yazi.toml

# 文件打开操作
[open]
rules = [
	# Folder - 目录规则
	{ name = "*/", use = ["edit", "open", "reveal"] },  # 目录：用编辑器打开/系统打开/在文件管理器中显示
	
	# Text - 文本文件规则
	{ mime = "text/*", use = ["edit", "reveal"] },  # 文本文件（.txt, .md, .py等）：用编辑器打开/在文件管理器中显示
	
	# Image - 图片文件规则
	{ mime = "image/*", use = ["open", "reveal"] },  # 图片文件（.jpg, .png等）：用系统默认程序打开/在文件管理器中显示
	
	# Media - 媒体文件规则
	{ mime = "{audio,video}/*", use = ["play", "reveal"] },  # 音频和视频文件：用播放器播放/在文件管理器中显示
	
	# Archive - 压缩文件规则
	{ mime = "application/{,g}zip", use = ["extract", "reveal"] },  # GZIP压缩文件：解压/在文件管理器中显示
	{ mime = "application/{tar,bzip*,7z*,xz,rar}", use = ["extract", "reveal"] },  # 其他压缩格式（tar, bzip2, 7z, xz, rar）：解压/在文件管理器中显示
	
	# JSON - JSON文件规则
	{ mime = "application/{json,ndjson}", use = ["edit", "reveal"] },  # JSON和NDJSON文件：用编辑器打开/在文件管理器中显示
	{ mime = "*/javascript", use = ["edit", "reveal"] },  # JavaScript文件：用编辑器打开/在文件管理器中显示
	
	# Empty file - 空文件规则
	{ mime = "inode/empty", use = ["edit", "reveal"] },  # 空文件（0字节）：用编辑器打开/在文件管理器中显示
	
	# Fallback - 默认/后备规则
	{ name = "*", use = ["edit", "open", "reveal"] },  # 其他所有文件：用编辑器打开/系统默认程序打开/在文件管理器中显示
]
