# Adb-Pull #

## 描述 ##

`Adb-Pull`包含一系列命令，可用来快速拷贝`/data/data/[PACKAGE]`目录下的内容至电脑本地。

注意：

1. **手机需要root**；
2. **目前只支持拷贝文件夹，不支持单个文件**；

## 安装 ##

执行以下命令：

	git clone git@github.com:naturs/adb-shell.git
	cd adb-shell/pull

	sudo cp ./adb-pull /usr/local/bin/
	sudo cp ./adb-pull-databases /usr/local/bin/
	sudo cp ./adb-pull-sharedpreferences /usr/local/bin/
	sudo cp ./adb-pull-files /usr/local/bin/
	sudo cp ./adb-pull-cache /usr/local/bin/
	sudo cp ./adb-pull-all /usr/local/bin/
	
	sudo chmod +x /usr/local/bin/adb-pull
	sudo chmod +x /usr/local/bin/adb-pull-databases
	sudo chmod +x /usr/local/bin/adb-pull-sharedpreferences
	sudo chmod +x /usr/local/bin/adb-pull-files
	sudo chmod +x /usr/local/bin/adb-pull-cache
	sudo chmod +x /usr/local/bin/adb-pull-all

## 使用 ##

导出`databases`目录：

	adb-pull-databases [YOUR_PACKAGE]

导出`shared_prefs`目录：

	adb-pull-sharedpreferences [YOUR_PACKAGE]

导出`files`目录：

	adb-pull-files [YOUR_PACKAGE]

导出`cache`目录：

	adb-pull-cache [YOUR_PACKAGE]

导出`/data/data/[YOUR_PACKAGE]`整个目录：

	adb-pull-all [YOUR_PACKAGE]

导出指定目录：

	adb-pull [YOUR_PACKAGE] databases            # 等同于adb-pull-databases [YOUR_PACKAGE]
	adb-pull [YOUR_PACKAGE] [folder1]/[folder2]  # 注意是[YOUR_PACKAGE]目录下的文件夹

## License ##

	Copyright 2017 naturs

	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at

	http://www.apache.org/licenses/LICENSE-2.0

	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.