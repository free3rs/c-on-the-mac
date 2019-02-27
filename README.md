# c-on-the-mac
c programing on osx 10.14


1.打开 Sublime Tools->Build System -> New Build System
2.粘贴下面json到 对应的区域 保存
{
    "cmd": ["gcc -Wall -o ${file_base_name} $file_name"],
    "shell": true,
    "working_dir": "$file_path",
    "selector": "source.c",
    "encoding": "utf-8",
    "variants": [{
        "name": "Run",
        "cmd": "./${file_base_name}"
    }, {
        "name": "BuildAndRun",
        "cmd": ["gcc -Wall -o ${file_base_name} $file_name && ./${file_base_name}"]
    }]
}
