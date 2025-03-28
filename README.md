Hello everyone, many of you probably know that using a search on github, you can find free working api keys from various services, for example, api keys from OpenAI, deepseek, etc., and I managed to make a couple of working filters for searching on github to find a lot of working keys, I certainly do not promise that everything will be fine. it works 100%, but you can try it if you want.
Also, while writing filters for search, I noticed that, for example, it is almost impossible to write a good filter for Mistral, since their keys seem to be completely random, so I don't have any ideas how to make filters for them yet, sorry.nt.

# [OpenAi](https://github.com/search?q=%22sk-%22+AND+%28openai+OR+%22api.openai.com%22%29+AND+%28++++%22%3D+%27sk-%22+OR++++%22%3D+%5C%22sk-%22+OR++++%22%3A+%5C%22sk-%22+OR++++%22%3A%5Cs*%5B%27%5C%22%5Dsk-%22+OR++++%22api_key%22+OR++++%22OPENAI_API_KEY%22+%29++-path%3A*.jsx+-path%3A*.tsx++AND+%28path%3A*.env+OR+path%3A*.json+OR+path%3A*.yaml+OR+path%3A*.yml+OR+path%3A*.txt+OR+path%3A.env+OR+path%3Aconfig%29&type=code)
```
"sk-" AND (openai OR "api.openai.com") AND ( 
  "= 'sk-" OR 
  "= \"sk-" OR 
  ": \"sk-" OR 
  ":\s*['\"]sk-" OR 
  "api_key" OR 
  "OPENAI_API_KEY"
) 
-path:*.jsx -path:*.tsx 
AND (path:*.env OR path:*.json OR path:*.yaml OR path:*.yml OR path:*.txt OR path:.env OR path:config)
```

# [Cohere](https://github.com/search?q=%28+++%28cohere_api_key+OR+COHERE_KEY+OR+%22cohere+api%22%29++++AND++++%2F%5BA-Z0-9%5D%7B40%7D%2F++++AND++++%28language%3Apython+OR+language%3Ajavascript+OR+language%3Ayaml%29+%29++NOT+language%3Amarkdown++NOT+path%3Atest++NOT+path%3Aexample++NOT+path%3Amock&type=code)
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

# [Gemini](https://github.com/search?q=%22AIzaSy%22+AND+%28gemini+OR+%22generativelanguage.googleapis.com%22%29+AND+path%3Asrc+AND+%28path%3A*.env+OR+path%3A*.json+OR+path%3A*.yaml+OR+path%3A*.yml+OR+path%3A*.txt+OR+path%3A.env+OR+path%3Aconfig%29&type=code)
```
"AIzaSy" AND (gemini OR "generativelanguage.googleapis.com") AND path:src AND (path:*.env OR path:*.json OR path:*.yaml OR path:*.yml OR path:*.txt OR path:.env OR path:config)
```

# [DeepSeek]()
```
W.I.P.
```

# [Anthropic]()
```
W.I.P.
```
