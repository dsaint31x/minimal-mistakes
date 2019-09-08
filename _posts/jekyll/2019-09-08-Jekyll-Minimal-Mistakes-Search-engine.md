---
title: "[Jekyll] Minimal-Mistakes에 Google custom search engine"
last_modified_at: 2019-09-08 22:00:00
categories: 
 - jekyll
 - minimal-mistakes
 - blogging
 - log4blog
use_math: false
tags: 
 - jekyll
 - custum search engine
toc: true
---

# Add Google Custom Search Engine to my blog

@(Jekyll,search engine)

Google Custom Search Engine은 구글의 검색기능을 사용자가 원하는 사이트에만 한정하여 검색하도록 지정된 검색엔진이다.
우선, Jekyll로 만든 사이트 뿐 아니라 거의 대부분의 경우 추가가 가능하지만 Jekyll의 minimal mistakes 테마에 추가하는 것만 간략히 살펴보고 내 블로그에 추가했다.

1. Edit `_config.yml` to enable site-wide search >
  add `search: true` and `search_provider : google`
2. Create a **New search engine(새검색엔진)** in [Google Custom Engine](https://cse.google.com/cse/all), enter it an appropriate name(검색엔진이름) and setup "Sites to search(검색할 사이트)"
3. Under **Edit search engine > Look and feel**, choose the **Results only** layout.
4. Select **Save & Get Code** and grab your search engine ID from the line that begins with `var cx = `YOUR_SEARCH_ENGINE_ID`.
5. Add your serach engine ID to `_config.yml` like so:
```ruby
google:
  search_engine_id: YOUR_SEARCH_ENGINE_ID
```

## Note
* The result provided from the GCSE includes the urls of advertisement.

## References

* [Configuration of Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#google-custom-search-engine)
