# adaptive-card-rs

[![Crates.io](https://img.shields.io/crates/v/adaptive-card-rs)](https://crates.io/crates/adaptive-card-rs)
[![Docs.rs](https://docs.rs/adaptive-card-rs/badge.svg)](https://docs.rs/adaptive-card-rs/latest/adaptive_card_rs/)

This crate provides the structures for building Adaptive Cards, which are designed to be
rendered in the Adaptive Card ecosystem. Adaptive Cards are used to create rich
interactive content in a structured way.

https://adaptivecards.io/

## Installation

Add this crate to your `Cargo.toml` to use it in your Rust project:

```sh
cargo add adaptive-card-rs
```

## Overview
 Adaptive Cards consist of:
 - A schema defining the version and structure.
 - A collection of card elements (e.g., TextBlock, Image, FactSet).
 - Optional actions that users can trigger.

 ```rust
 use adaptive_card_rs::card::{AdaptiveCard, Version, CardElement, TextBlock, TextSize, TextWeight};

 let card = AdaptiveCard {
     version: Version::V1_3,
     body: vec![
         CardElement::TextBlock(TextBlock {
             size: Some(TextSize::Large),
             weight: Some(TextWeight::Bolder),
             text: "Hello, Adaptive Card!".to_string(),
             wrap: Some(true),
             is_subtle: Some(false),
         })
     ],
 ..Default::default()
 };
 ```
