---
layout: post
title: "Writing Files Through Shell"
published: true
tags: [Bash, Shell, Unix]
---


# Writing to file in Bash

    cat >/my/path.extension <<EOL
    line 1,
    line 2,
    line 3,
    line 4 line
    ...
    EOL

## Another thing about cat:

cat > file **writes** to file*
cat >> file **appends** to file*
