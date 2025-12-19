# Chat Stream

An Obsidian plugin for conversing with LLMs canvas notes. Ancestor notes/files are included in the chat context. You can quickly create chat streams, and control what other notes are sent to the LLM.

<img src="static/chat-stream-example.gif"/>

## Install

Install as [community plugin](https://obsidian.md/plugins?search=chat%20stream#)

Add `mounta11n/canvas-stream` to [BRAT](https://github.com/TfTHacker/obsidian42-brat).

Chat Stream is supported only on desktop.

## Usage

1. Select a note in the canvas
2. Press Option+Shift+G or Alt+Shift+G to generate new note from LLM using current note + ancestors
3. To create next note for responding, press Option+Shift+N or Alt+Shift+N.

LLM's notes are colored purple, and tagged with `chat_role=assistant` in the canvas data file.

## Development

1. Download source and install dependencies
   ```
	bun install
	```
2. In Obsidian, install and enable [hot reload plugin](https://github.com/pjeby/hot-reload)
3. Create symbolic link from this project dir to an Obsidian store 
   ```
	ln -s $(pwd) <your-obsidian-store>/.obsidian/plugins/canvas-stream
	```
4. Start dev server
	```
	bun run dev
	```
5. In Obsidian, enable Chat Stream Plugin and add OpenAI key in plugin settings.

Changes to code should automatically be loaded into Obsidian.

6. Or build the plugin
   ```
	bun run build
   ```   

## Attribution

* Canvas plugin code from [Canvas MindMap](https://github.com/Quorafind/Obsidian-Canvas-MindMap)
