---
layout: post
title: PyPi and RubyGems mirrors in China
date: August 07, 2014
category: tips
customid: 22kt3gkhgy5kwjfhy9e38
---

## PyPi

```bash
mkdir -p ~/.pip
touch ~/.pip/pip.conf
sed -i.backup -r \
    's/^index-url\s*=\s*.+$/index-url = http:\/\/mirrors.aliyun.com\/pypi\/simple\//' \
    ~/.pip/pip.conf
# If file not changed, write contents back to pip.conf
diff "~/.pip/pip.conf" "~/.pip/pip.conf.backup" &> /dev/null
if [ $? -eq 0 ]; then
cat > ~/.pip/pip.conf <<EOF
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
EOF
fi
```

## RubyGems

```bash
gem source -r https://rubygems.org/
gem source -a http://mirrors.aliyun.com/rubygems/

```
