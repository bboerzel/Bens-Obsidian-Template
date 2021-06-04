<%*
const choices = [
        
		{option: "✔ Task ", 
		captureTo: "001 ToDo", 
		task: true,
		insertAfter: "# Inbox", 
		format: "{{VALUE}} 📆: [[{{DATE}}]] ✔️: \n"},
		
		{option: "💭 Thought ", 
		captureTo: "002 Top of Mind", 		
		prepend: true,
		format: "📆[[{{DATE}}]]  {{VALUE}}"
		},
				        
		{option: "📆 New Meeting ", 
		format: `📆{{DATE:gggg-MM-DD}}  {{NAME}}`, 
		folder: "07📆 Journal/", 
		path: "Templates/TMP Meeting.md"
		},
       
	   {option: "🧑 Person ", 
		format: `@{{NAME}}`, 
		folder: "09🧑 People/", 
		path: "Templates/TMP People.md"
		},	
	
		{option: "💡 Bit ", 
		format: `{{NAME}}`, 
		folder: "02💡 Bits/", 
		path: "Templates/TMP bit.md",
		appendLink: true,
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "🌍 Source ", 
		format: `{{NAME}}`, 
		folder: "04🌍 Sources/", 
		path: "Templates/TMP Source.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "🧰 Knowledge Base", 
		format: `{{NAME}}`, 
		folder: "03🧰 KnowledgeBase/", 
		path: "Templates/TMP Knowledge Base.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "👩‍💻 Snippet", 
		format: `{{NAME}}`, 
		folder: "03🧰 KnowledgeBase/", 
		path: "Templates/TMP Snippet.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "🔖Read Later", 
		captureTo: "091 Read Later", 		
		prepend: true,
		task: true,
		format: "{{VALUE}} 📆[[{{DATE}}]]"
		},
		

]

const out = await tp.user.QuickAdd(tp, choices);
if (out) tR = out;
%>