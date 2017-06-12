---
title: hyper.rs
layout: home
---


<section class="jumbotron hyper-pageheader">
  <div class="container">
    <h1 class="hyper-logo">hyper</h1>
    <p>Fast and safe HTTP for the Rust language.</p>
    <!--
    <p><a href="/guides" class="btn hyper-getstarted">Get Started</a></p>
    -->
  </div>
</section>
<section class="container">
<div class="row">
  <div class="col-md-6">
    <h1>hyper <small>typed http</small></h1>
    <p class="lead">Hyper is a fast HTTP implementation written in and for Rust.</p>
    <p>It is a low-level typesafe abstraction over raw HTTP, providing an elegant layer over "stringly-typed" HTTP.</p>
    <p>Hyper offers both an HTTP client and server which can be used to drive complex web applications written entirely in Rust.</p>
    <p><a class="btn btn-primary" href="https://hyperium.github.io/hyper">Documentation</a></p>
  </div>
  <div class="col-md-6">
    <h2>Installation</h2>
    <div class="card">
      <div class="card-header">Cargo.toml</div>
      <div class="card-block">
        <pre><code>[dependencies]
hyper = "0.10"
        </code></pre>
      </div>
    </div>
  </div>
  <!--
  <div class="col-md-6">
    <h2>Hello, World</h2>
    <div class="card">
      <div class="card-header"></div>
      <div class="card-block" markdown="1">

```rust
extern crate hyper;
extern crate service_fn;

use hyper::header::{ContentLength, ContentType};
use hyper::server::{Http, Response};
use service_fn::service_fn;

static TEXT: &'static str = "Hello, World!";

fn run() -> Result<(), hyper::Error> {
    let addr = ([127, 0, 0, 1], 3000).into();

    let hello = |_req| {
        Ok(Response::new()
            .with_header(ContentLength(TEXT.len() as u64))
            .with_header(ContentType::plaintext())
            .with_body(TEXT))
    };

    let server = Http::new().bind(addr, || Ok(service_fn(hello)))?;
    server.run()?;

    Ok(())
}

fn main() {
    run().expect("Server error");
}
```

      </div>
    </div>
  </div>
  -->

</div>
</section>