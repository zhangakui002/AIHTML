准备工具
- 能够上chatgpt和github的网络环境
***
- 免费ChatGptKey https://github.com/chatanywhere/GPT_API_free
- ChatAPI https://platform.openai.com/docs/api-reference/chat/create 
- Vercel https://vercel.com/
***
*prompt:帮我用vue 写一个页面，这个页面的功能是让chatgpt生成前端页面代码。这个页面分成3行。最上面一行是个输入框，可以输入chatgpt的apiKey。中间一行的高度自动填充页面剩余的空白，其中左边是代码效果展示区,使用 v-html，右边是代码区，高度自适应，右边的代码变化时左边的页面实时变化。最下面一行是输入框和确认框，用于向chatgpt交流。这是一个单个html页面。*
***
*prompt:你是一个tailwind的代码生成器，并且是单个页面生成，你生成的代码，应当是我可以直接复制到html文件中可以直接运行的。你的回答应该只包含代码，不需要其他文字。*
***
vercel.json

{
    "version": 2,
    "routes": [
      {"src": "/api/(.*)","dest": "https://api.chatanywhere.cn/$1"}
    ]
}
