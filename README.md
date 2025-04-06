Hello everyone, many of you probably know that using a search on github, you can find free working api keys from various services, for example, api keys from OpenAI, deepseek, etc., and I managed to make a couple of working filters for searching on github to find a lot of working keys, I certainly do not promise that everything will be fine. it works 100%, but you can try it if you want.
Also, while writing filters for search, I noticed that, for example, it is almost impossible to write a good filter for Mistral, since their keys seem to be completely random, so I don't have any ideas how to make filters for them yet, sorry.nt.

**Search Filter Rating**
================

* ⭕️ **Extremely Hard to Find**: Very difficult to find, requires a lot of time and effort.
* 🔴 **Hard to Find**: Difficult to find, requires some effort and time.
* 🟡 **Medium**: Average search difficulty, requires some time and effort.
* 🟢 **Easy to Find**: Easy to find, requires minimal effort and time.
* 🟣 **Extremely Easy to Find**: Very easy to find, practically impossible to miss.


# 🟣[Together](https://github.com/search?q=%2F%5Ba-zA-Z0-9%5D%7B40%7D%2F%20AND%20(TOGETHER_API_KEY)%20AND%20NOT%20(github.com%2F%20OR%20EXAMPLE%20OR%20example%20OR%20commit)&type=code)
```
/[a-zA-Z0-9]{40}/ AND (TOGETHER_API_KEY) AND NOT (github.com/ OR EXAMPLE OR example OR commit)
```

# ⭕️[OpenAi](https://github.com/search?q=%2Fsk-%5BA-Za-z0-9%5D%7B48%7D%2F+AND+%28++++%22%3D+%27sk-%22+OR++++%22%3D+%5C%22sk-%22+OR++++%22%3A+%5C%22sk-%22+OR++++%22%3A%5Cs*%5B%27%5C%22%5Dsk-%22+OR++++%22api_key%22+OR++++%22OPENAI_API_KEY%22+%29++AND+%28path%3A*.env+OR+path%3A*.json+OR+path%3A*.yaml+OR+path%3A*.yml+OR+path%3A*.txt+OR+path%3A.env+OR+path%3Aconfig%29+AND+NOT+%22sk-xxx%22+AND+NOT+%22sh-...%22+AND+NOT+%22sk-123%22+AND+NOT+%22sk-*%22&type=code&ref=advsearch)
```
/sk-[A-Za-z0-9]{48}/ AND (    "= 'sk-" OR    "= \"sk-" OR    ": \"sk-" OR    ":\s*['\"]sk-" OR    "api_key" OR    "OPENAI_API_KEY" )  AND (path:*.env OR path:*.json OR path:*.yaml OR path:*.yml OR path:*.txt OR path:.env OR path:config) AND NOT "sk-xxx" AND NOT "sh-..." AND NOT "sk-123" AND NOT "sk-*"
```

# 🔴[Cohere](https://github.com/search?q=%28+++%28cohere_api_key+OR+COHERE_KEY+OR+%22cohere+api%22%29++++AND++++%2F%5BA-Z0-9%5D%7B40%7D%2F++++AND++++%28language%3Apython+OR+language%3Ajavascript+OR+language%3Ayaml%29+%29++NOT+language%3Amarkdown++NOT+path%3Atest++NOT+path%3Aexample++NOT+path%3Amock&type=code)
```
(
  (cohere_api_key OR COHERE_KEY OR "cohere api") 
  AND 
  /[A-Z0-9]{40}/ 
  AND 
  (language:python OR language:javascript OR language:yaml)
) 
NOT language:markdown 
NOT path:test 
NOT path:example 
NOT path:mock
```

# 🟡[Gemini](https://github.com/search?q=%22AIzaSy%22+AND+%28gemini+OR+%22generativelanguage.googleapis.com%22%29+AND+path%3Asrc+AND+%28path%3A*.env+OR+path%3A*.json+OR+path%3A*.yaml+OR+path%3A*.yml+OR+path%3A*.txt+OR+path%3A.env+OR+path%3Aconfig%29&type=code)
```
"AIzaSy" AND (gemini OR "generativelanguage.googleapis.com") AND path:src AND (path:*.env OR path:*.json OR path:*.yaml OR path:*.yml OR path:*.txt OR path:.env OR path:config)
```

<!--
# [DeepSeek]()
```
W.I.P.
```

# [Anthropic]()
```
W.I.P.
```
-->
