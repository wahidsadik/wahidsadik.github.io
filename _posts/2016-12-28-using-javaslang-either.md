---
layout: post
title:  "Using Javaslang Either"
categories: coding
tags: [java8, functional]
---

As more and more codebases are migrated to Java 8, I am taking advantage of functional approach. [Javaslang](http://www.javaslang.io/) adds to the power of Java's out-of-the-box capabilities. On of these features is [Either](http://static.javadoc.io/io.javaslang/javaslang/2.1.0-alpha/index.html?javaslang/control/Either.html).

`Either` allows to a convenient way of returning two different types of responses from a method. There are `Either.right` and `Either.left`.

Typical use case - Imagine a method returning some collection on success and an exception on error. We can substitute the exception part with an enum/String when we use `Either`. By convention, with `Either.right` refers to success.

The following code should help understand the usage.

**Code**

````
package com.wahid.javaslang.demo;

import java.util.List;

import com.google.common.collect.Lists;
import javaslang.control.Either;

public class UsingEither {

  public Either<String, List<String>> soSomething(int param) {
    if(param == 1) {
      return Either.right(Lists.newArrayList("got one"));
    } else {
      return Either.left("param != 1");
    }
  }
}

````

**Test**
````
package com.wahid.javaslang.demo;

import static org.junit.Assert.assertEquals;
import static org.junit.Assert.assertTrue;

import java.util.List;

import javaslang.control.Either;
import org.junit.Test;

public class UsingEitherTest {

  private UsingEither underTest = new UsingEither();

  @Test
  public void testEither() {
    Either<String, List<String>> either1 = underTest.soSomething(1);
    assertTrue(either1.isRight());
    assertTrue(either1.get() instanceof List);
    assertEquals("got one", either1.get().get(0));

    Either<String, List<String>> either2 = underTest.soSomething(2);
    assertTrue(either2.isLeft());
    assertTrue(either1.get() instanceof String);
    assertEquals("param != 1", either2.getLeft());
  }

}
````
