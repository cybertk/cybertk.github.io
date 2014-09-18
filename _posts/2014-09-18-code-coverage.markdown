---
layout: post
title: code coverage
date: September 18, 2014
category: test
customid: 1tl4nsafud52xbtzqa3mi
---

Code Coverage, it basically just has a counter for each line that gets increased whenever execution passes it.

#### gcov

gcov is popular tool for record code coverage, which generate

- GCNO, generated when the source file is compiled.
- GCDA, generated in runtime when code pass.

#### GCDA

GCDA is a binary format for which we need to have a viewer application to make sense of.

- [coverstory][], for mac
- [coveralls][], online

[coverstory]: https://code.google.com/p/coverstory/

#### lcov

#### Refs

- [xcode-coverage][1]
- [Coveralls-iOS][2]
- [xcode-code-coverage][3]


[1]: http://www.cocoanetics.com/2013/10/xcode-coverage/
[2]: https://github.com/azu/Coveralls-iOS
[3]: http://qualitycoding.org/xcode-code-coverage/
