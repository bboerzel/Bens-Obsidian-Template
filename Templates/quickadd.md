<%*
const choices = [
        
		{option: "β Task ", 
		captureTo: "001 ToDo", 
		task: true,
		insertAfter: "# Inbox", 
		format: "{{VALUE}} π: [[{{DATE}}]] βοΈ: \n"},
		
		{option: "π­ Thought ", 
		captureTo: "002 Top of Mind", 		
		prepend: true,
		format: "π[[{{DATE}}]]  {{VALUE}}"
		},
				        
		{option: "π New Meeting ", 
		format: `π{{DATE:gggg-MM-DD}}  {{NAME}}`, 
		folder: "07π Journal/", 
		path: "Templates/TMP Meeting.md"
		},
       
	   {option: "π§ Person ", 
		format: `@{{NAME}}`, 
		folder: "09π§ People/", 
		path: "Templates/TMP People.md"
		},	
	
		{option: "π‘ Bit ", 
		format: `{{NAME}}`, 
		folder: "02π‘ Bits/", 
		path: "Templates/TMP bit.md",
		appendLink: true,
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "π Source ", 
		format: `{{NAME}}`, 
		folder: "04π Sources/", 
		path: "Templates/TMP Source.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "π§° Knowledge Base", 
		format: `{{NAME}}`, 
		folder: "03π§° KnowledgeBase/", 
		path: "Templates/TMP Knowledge Base.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "π©βπ» Snippet", 
		format: `{{NAME}}`, 
		folder: "03π§° KnowledgeBase/", 
		path: "Templates/TMP Snippet.md",
		noOpen: false,
		newTab: "vertical"
		},
		
		{option: "πRead Later", 
		captureTo: "091 Read Later", 		
		prepend: true,
		task: true,
		format: "{{VALUE}} π[[{{DATE}}]]"
		},
		

]

const out = await tp.user.QuickAdd(tp, choices);
if (out) tR = out;
%>