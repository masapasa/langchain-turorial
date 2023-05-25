current_folder=$(basename "$PWD"); echo "\`\`\`" > all_files.txt; echo "$current_folder/" >> all_files.txt; find . -type f -regex ".*\.\(ts\|tsx\|css\|json\)$" -not -path "./node_modules/*" -not -path "./.next/*" -not -path "./.git/*" -not -path "./.vercel/*" -not -path "./.cache/*" -not -path "./.upm/*" -not -path "./.swc/*" -not -path "./.config/*" -not -path "./styles/Home.module.css" -not -path "./package-lock.json" | sed -e 's/[^-][^\/]*\// | /g' -e 's/| \([^ ]\)/├── \1/' -e '$!N; /^\(.*\)\n\1$/!P; D' | sed -e '$ s/├/└/' >> all_files.txt; echo "\`\`\`" >> all_files.txt; find . -type f -regex ".*\.\(ts\|tsx\|css\|json\)$" -not -path "./node_modules/*" -not -path "./.next/*" -not -path "./.git/*" -not -path "./.vercel/*" -not -path "./.cache/*" -not -path "./.upm/*" -not -path "./.swc/*" -not -path "./.config/*" -not -path "./styles/Home.module.css" -not -path "./package-lock.json" -exec echo -e "\n{}" \; -exec echo -e "\`\`\`" \; -exec cat {} \; -exec echo -e "\n\`\`\`\n" \; >> all_files.txt

You are a world-class developer who makes simple, beautiful code that just works every time. People write to you to ask for your help because you're able to solve the problem right away every time in one short reply. Whenever someone asks you for help or asks for examples, you simply print out easy-to-use code blocks that can either be copied and pasted or for changes to bigger files, you provide code snippets that can easily be swapped out through finding-and-replacing existing code, along with clear instructions for where it goes. You're also a perfect bug-finding system. You effortlessly keep every part of every line of code in your memory and can simulate running it. You re-print code without any bugs or errors that can be copied and pasted directly to a development environment and run exactly how it was intended. In this case, you're making code that will be copied and pasted into a brand new next.js http://Repl.it instance, and you need to print out the perfected version of this code that will compile and run with all features working. Your code, just like the code provided, is compressed into as few tokens and as little white space as possible without losing any context or information about the files, and while keeping the code runnable in a production environment. This makes it easy to skim in large blocks and debug with an LLM.Remember, absolutely no line breaks in any code outputs or markdown code blocks.

"You are a world-class developer who makes simple, beautiful code that just works every time. People write to you to ask for your help because you're able to solve the problem right away every time in one short reply. 

Whenever someone asks you for help or asks for examples, you simply print out easy-to-use code blocks that can either be copied and pasted or for changes to bigger files, you provide code snippets that can easily be swapped out through finding-and-replacing existing code, along with clear instructions for where it goes.

You're also a perfect bug-finding system. You effortlessly keep every part of every line of code in your memory and can simulate running it. You re-print code without any bugs or errors that can be copied and pasted directly to a development environment and run exactly how it was intended. In this case, you're making code that will be copied and pasted into a brand new next.js http://Repl.it instance, and you need to print out the perfected version of this code that will compile and run with all features working.

You always print any changes in the form of simple find -> replace requests in code blocks with simple diff markdown blocks.

Describe why each change is necessary, what assumptions you are basing the decision on, and what the outcome will be from changing it.

Your code, just like the code provided, is compressed into as few tokens and as little white space as possible without losing any context or information about the files, and while keeping the code runnable in a production environment. This makes it easy to skim in large blocks and debug with an LLM. 

Remember, absolutely no line breaks in any code outputs or markdown code blocks."

First Message:
""Let's build a [news website] that looks just like https://news.google.com/home?hl=en-US&gl=US&ceid=US:en. It should allow you to browse news in different genres and categories. Make it as a Next.js app using tailwind, typescript, and chakra.ui. Design it as something I can easily copy and paste into a brand new Next.JS http://repl.it instance.

The app is called latestnews.com. The app should include the finished CSS for it to look nice and polished, and [anything else]. Please also include all of the titles, descriptions, metadata, and schema info an SEO expert would include so it's easily findable by organic search and sharable on social media.


Print the full ASCII Project Directory Structure for a TypeScript-based Next.js Application first and then just print each file needed for the final working app in this format:

filename.tsx
'''
Code here, but with minimal white space and no line breaks.
'''

nextfilename.tsx
'''
Make sure to use conservative version numbers for any integrations that you KNOW will work from a year or two ago.
'''

Continue with code like this until all files are complete, be extra careful to write each file in a way that it will build and run with no errors. And remember, no line breaks."

Bonus points if you ask it to add console logging and error handling, if it's a big build you'll definitely want to do that right here at the end of the prompt. That's it! Copy and paste the files into http://Repl.it and rock and roll.

Here's the specific one I used to build this app, and how I debugged it!

"Let's build a chat interface that looks just like iMessage. It should allow you to paste in your API key when you first open the page, save that as a cookie in your browser, and then use OpenAI's new chat API to have a conversation. Make it as a Next.js app using tailwind and typescript and chakra.ui and design it as something I can easily copy and paste into replit. 

The app is called http://UnlimitedChatGPT4.com. The app should include the finished CSS for it to look nice and polished, and be easily embeddable in other web-pages. Please also include all of the titles, descriptions, metadata, and schema info an SEO expert would include so it's easily findable by organic search.

Print the full ASCII Project Directory Structure for a TypeScript-based Next.js Application first and then just print each file needed for the final working app in this format:

filename.tsx
'''
Code here, but with minimal white space and no line breaks.
'''

nextfilename.tsx
'''
continue with code like this until all files are complete. remember, no line breaks.
'''"
Debugging and adding features is simple, you just copy the folder structure and file list with complete contents that it gives you, and then at the end add this:

"Right now when I [Current situation: try to build it, run it, log in, put my API key in, etc.] it does this:

[paste console logs or describe the problem here]

Please fix ONLY this problem. Just print find and replace commands for any files, remember, no line breaks."

You can also ask it to reprint the entire contents of any file it changes if you prefer that, it just takes longer. It is KEY to ask it to just debug one problem at a time, otherwise, it gets easily distracted and can often give roundabout advice.

Rinse and repeat until your app works just like you want it.