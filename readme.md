# @silvenon/remark-smartypants

[remark] plugin to implement [SmartyPants].

```sh
npm install @silvenon/remark-smartypants
```

```js
const remark = require('remark')
const smartypants = require('@silvenon/remark-smartypants')

const content = remark()
  .use(smartypants)
  .processSync('# "Hello World!"')

console.log(String(content))
// # “Hello World!”
// (notice smart quotes)
```

"Why?" I hear nobody ask. Because I wanted to implement SmartyPants in [MDX]:

```js
const mdx = require('@mdx-js/mdx')
const smartypants = require('@silvenon/remark-smartypants')

const result = mdx('# "Hello World!"', {
  remarkPlugins: [
    smartypants,
  ],
})
```

[remark]: https://remark.js.org
[SmartyPants]: https://daringfireball.net/projects/smartypants
[MDX]: https://mdxjs.com
