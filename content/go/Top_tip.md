+++
date = "2016-05-20T11:06:58+08:00"
draft = true
title = "Go top tip collections"

+++


Go top tip collections.

- Put $GOPATH/bin in your $PATH, so installed binaries are easily accessible.
- If your repo foo is primarily a binary, put your library code in a lib/ subdir, and call it package foo. 
- If your repo is primarily a library, put your binaries in separate subdirectories under cmd/.
- [Idiomatic naming conventions](https://talks.golang.org/2014/names.slide)
- Only func main has the right to decide which flags are available to the user. 

<!--more-->

- Use struct literal initialization to avoid invalid intermediate state. Inline struct declarations where possible. 
- Avoid nil checks via default no-op implementations. 
- Make the zero value useful, especially in config objects. 
- Make dependencies explicit! 
- Loggers are dependencies, just like references to other components, database handles, commandline flags, etc.
- Use many small interfaces to model dependencies.
- Tests only need to test the thing being tested.
- Use a top tool to vendor dependencies for your binary.
- Libraries should never vendor their dependencies. 
- Prefer go install to go build.

- Time package tip: t1 := time.Now(); do_something(); d := time.Since(t1)
- Embedding can trigger unexpected, implicit indirection. Unless you know you need to embed, prefer naming your struct fields.
- Never launch a goroutine without knowing how and when it will stop.
- Mixing struct initialization with constructors ends badly. Once your type has a constructor, use it everywhere.
- Duplication is far cheaper than the wrong abstraction
- When a function takes a slice of T, prefer ...T over []T.
- Stop writing '%s' and start writing %q — https://golang.org/pkg/fmt.

Reference:

- https://peter.bourgon.org/go-best-practices-2016/
