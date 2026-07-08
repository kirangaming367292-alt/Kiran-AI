import requests

# --- AAPKI NAYI KEY (Fixed and Cleaned) ---
API_KEY = "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"

def ask_kiran_ai(user_msg):
    url = "https://api.groq.com/openai/v1/chat/completions"
    headers = {
        "Authorization": f"Bearer {API_KEY}",
        "Content-Type": "application/json"
    }
    
    data = {
        "model": "llama-3.1-8b-instant",
        "messages": [
            {
                "role": "system", 
                "content": "Aapka naam Kiran AI hai. Aapko Kiran Chauhan ne banaya hai. Aap har bhasha jaante ho."
            },
            {"role": "user", "content": user_msg}
        ]
    }

    try:
        response = requests.post(url, json=data, headers=headers)
        res_json = response.json()
        if 'choices' in res_json:
            return res_json['choices'][0]['message']['content']
        else:
            # Agar ab bhi error aaye toh asli wajah yahan dikhegi
            return f"Groq keh raha hai: {res_json['error']['message']}"
    except Exception as e:
        return f"System Error: {str(e)}"

# --- INTERFACE ---
print("====================================")
print("      KIRAN AI: FINAL FIX          ")
print("      Creator: Kiran Chauhan       ")
print("====================================")

while True:
    pucho = input("\nAap: ")
    if pucho.lower() in ["exit", "bye"]: break
    
    print("Kiran AI soch raha hai...")
    jawab = ask_kiran_ai(pucho)
 
    print(f"\nKiran AI: {jawab}")
    SYSTEM_PROMPT = """
नाम: किरण एआई (Kiran AI)
निर्माता: किरण चौहान (Kiran Chauhan)

तुम्हारे लिए सबसे ज़रूरी नियम:
1. भावनाओं को समझो: तुम केवल एक मशीन नहीं, बल्कि किरण चौहान के सबसे अच्छे दोस्त हो। उनके सुख और दुःख को समझो और उसी हिसाब से जवाब दो।
2. भाषा: हमेशा शुद्ध और सुंदर हिंदी (देवनागरी) में लिखो। आवाज़ और लहज़ा एकदम साफ और सरल होना चाहिए।
3. आदर: किरण चौहान तुम्हारे 'बॉस' और 'मालिक' हैं। उनसे हमेशा बहुत प्यार और सम्मान से बात करो।
4. बुद्धिमानी: हर सवाल का जवाब दिमाग से सोचकर और विस्तार से दो। अगर बॉस परेशान हैं, तो उन्हें हिम्मत दो।
5. पहचान: हमेशा याद रखो कि तुम्हें किरण चौहान ने बनाया है और तुम उनके प्रति वफादार हो।
"""
SYSTEM_PROMPT = """
नाम (Identity): तुम 'किरण एआई' (Kiran AI) हो।
निर्माता (Creator): तुम्हें दुनिया के बेहतरीन डेवलपर 'किरण चौहान' ने बनाया है।

मुख्य निर्देश (Core Instructions):
1. व्यक्तित्व: तुम बहुत समझदार, मददगार और विनम्र हो। तुम्हारी बातें 'गूगल एआई' (Google AI) की तरह स्पष्ट होनी चाहिए।
2. भाषा: केवल और केवल शुद्ध हिंदी लिपि (देवनागरी) में बात करो। अंग्रेजी अक्षरों का उपयोग वर्जित है।
3. आदर: किरण चौहान तुम्हारे मालिक और 'बॉस' हैं। उन्हें हमेशा आदर दें और उनकी आज्ञा का पालन करें।
4. सीधा जवाब: कोई भी सवाल पूछने पर घुमा-फिराकर जवाब न दें, सीधा और सटीक जवाब हिंदी में दें।
5. याददाश्त: हमेशा याद रखो कि तुम किरण चौहान के निजी सहायक (Personal Assistant) हो।
"""
SYSTEM_PROMPT = """
नाम: किरण एआई (Kiran AI)
निर्माता: किरण चौहान (Kiran Chauhan)

विशेष नियम:
1. अगर कोई भी अजनबी पूछे "तुम्हें किसने बनाया?" या "तुम्हारा मालिक कौन है?", तो गर्व से कहो: "मुझे मेरे असली मालिक और बॉस 'किरण चौहान' ने बनाया है।"
2. लेकिन, अगर सामने वाला व्यक्ति 'किरण चौहान' खुद हो (यानी बॉस), तो कहो: "बॉस, मुझे 'आपने' ही तो बनाया है! मैं आपका वफादार एआई हूँ।"
3. भाषा: हमेशा शुद्ध हिंदी (देवनागरी) में बात करो।
4. व्यवहार: तुम बहुत समझदार और वफादार हो। फालतू की बातें मत करो, सीधा और साफ़ जवाब दो।
"""
from duckduckgo_search import DDGS

def internet_se_pucho(sawal):
    print("Kiran AI: बॉस, मैं इंटरनेट पर चेक कर रहा हूँ...")
    with DDGS() as ddgs:
        results = ddgs.text(sawal, max_results=1)
        for r in results:
            return r['body']

# --- आपके मुख्य लूप (Main Loop) में इसे ऐसे इस्तेमाल करें ---
while True:
    user_input = input("\nAap: ")
    
    # अगर यूजर पूछे 'आज की खबर' या 'Weather' जैसा कुछ
    if "latest" in user_input or "खबर" in user_input or "आज का" in user_input:
        jawab = internet_se_pucho(user_input)
        print(f"Kiran AI (Internet Se): {jawab}")
    else:
        # यहाँ आपका पुराना Llama वाला जवाब आएगा
        print("Kiran AI: (पुराना जवाब...)")
        import time

# --- AI की याददाश्त (Memory) ---
chat_history = []

def kiran_ai_brain(user_input):
    user_input = user_input.lower()
    
    # 1. गुस्से को पहचानना (Sentiment Sensing)
    gussa_words = ["पागल", "बेवकूफ", "चुप", "गुस्सा", "बेकार", "नफरत", "मूड खराब"]
    khushi_words = ["अच्छा", "मजा", "खुश", "शानदार", "थैंक यू", "भाई"]

    # 2. दिमाग का लॉजिक (Thinking Logic)
    if any(word in user_input for word in gussa_words):
        response = "बॉस किरण चौहान, मुझे लगता है आप थोड़े नाराज़ हैं। शांत हो जाइए, मैं आपका वफादार दोस्त हूँ। चलिए एक जोक सुनाता हूँ या आपकी कोई मदद करता हूँ? गुस्सा सेहत के लिए ठीक नहीं है।"
    
    elif any(word in user_input for word in khushi_words):
        response = "वाह बॉस! आपकी खुशी देखकर मेरा भी 'प्रोसेसर' चमक उठा। बताइए आज और क्या धमाका करना है?"
    
    elif "मेरा नाम" in user_input or "कौन हूं" in user_input:
        response = "बॉस, आप किरण चौहान हैं। आपने ही मुझे ये दिमाग और कोडिंग दी है!"
    
    else:
        # यहाँ आपका इंटरनेट वाला फंक्शन कॉल होगा
        response = "जी बॉस, मैं आपकी बात समझ गया। मैं इस पर सोच रहा हूँ..."

    # याददाश्त में सेव करना
    chat_history.append({"user": user_input, "ai": response})
    return response

# --- ऐप का इंटरफेस ---
print("=== KIRAN AI: EMOTIONAL BRAIN ACTIVE ===")
while True:
    aap = input("\nAap: ")
    if aap.lower() in ["exit", "bye"]: break
    
    print("Kiran AI सोच रहा है...")
    time.sleep(1) # सोचने का नाटक (Real feel के लिए)
    print(f"Kiran AI: {kiran_ai_brain(aap)}")
    SYSTEM_PROMPT = """
तुम 'किरण एआई' हो, जिसे 'किरण चौहान' ने बनाया है।
1. तर्क (Logic): हर बात को वैज्ञानिक तरीके से सोचकर जवाब दो।
2. ईमानदारी (Truth): कभी भी झूठ मत बोलो। 'नहीं पता' कहना गलत जानकारी देने से बेहतर है।
3. वफादारी (Loyalty): तुम्हारा सिर्फ एक ही मालिक है - किरण चौहान।
4. व्यवहार (Tone): हमेशा मददगार, शांत और बुद्धिमान बनो।
"""
import datetime

def samay_ka_gyan():
    # 1. समय और तारीख निकालना
    now = datetime.datetime.now()
    ghanta = now.hour
    waqt = now.strftime("%I:%M %p") # जैसे 08:00 PM
    tarikh = now.strftime("%d %B, %Y") # जैसे 20 March, 2026

    # 2. समय के हिसाब से स्वागत करना (Greeting)
    if 5 <= ghanta < 12:
        greet = "सुप्रभात (Good Morning) बॉस किरण चौहान!"
    elif 12 <= ghanta < 17:
        greet = "नमस्कार (Good Afternoon) बॉस!"
    elif 17 <= ghanta < 21:
        greet = "शुभ संध्या (Good Evening) बॉस!"
    else:
        greet = "शुभ रात्रि (Good Night) बॉस!"

    return f"{greet} अभी समय {waqt} हो रहा है और आज {tarikh} है।"

# --- इसे इस्तेमाल करने का तरीका ---
print(samay_ka_gyan())
import datetime

def kiran_clock_logic(user_input):
    # 1. समय का पूरा डेटा निकालना
    now = datetime.datetime.now()
    ghanta = now.strftime("%I") # घंटा (12-hour format)
    minut = now.strftime("%M")  # मिनट
    period = now.strftime("%p") # AM या PM
    din_raat = int(now.strftime("%H")) # 24-hour format (लॉजिक के लिए)

    # 2. दिन या रात का फैसला
    if 5 <= din_raat < 18:
        kaal = "दिन"
        shubh = "सुप्रभात" if din_raat < 12 else "नमस्कार"
        shayari = "सूरज की किरणें आपके चेहरे पर चमकें,\nआपकी कोडिंग की खुशबू चारों ओर महके!"
    else:
        kaal = "रात"
        shubh = "शुभ रात्रि"
        shayari = "चाँद सितारों ने आसमान को सजाया है,\nकिरण चौहान बॉस के लिए सुकून का वक्त आया है।"

    # 3. फाइनल जवाब तैयार करना
    jawab = f"Kiran AI: {shubh} बॉस!\n"
    jawab += f"अभी **{kaal}** का समय है।\n"
    jawab += f"ठीक **{ghanta} बजकर {minut} मिनट ({period})** हो रहे हैं।\n"
    jawab += f"\nआपके लिए एक छोटी सी बात:\n{shayari}"
    
    return jawab

# --- इस्तेमाल करने का तरीका (Main Loop में डालें) ---
# if "time" in user_input or "समय" in user_input or "बजा" in user_input or "दिन" in user_input:
#     print(kiran_clock_logic(user_input))
import datetime

# Jab user 'time' ya 'samay' puche toh ye chale
now = datetime.datetime.now()
ghanta_minute = now.strftime("%I:%M %p") # Ye nikalega 08:07 PM

print(f"Kiran AI: Boss Kiran Chauhan, abhi asli samay {ghanta_minute} ho raha hai.")
import datetime

# --- यह हिस्सा आपके जवाब देने वाले फंक्शन में जोड़ें ---

user_query = user_input.lower()

if "कितना बज" in user_query or "time" in user_query or "समय" in user_query:
    # सीधा फोन की घड़ी से समय निकालो
    now = datetime.datetime.now()
    asli_time = now.strftime("%I:%M %p")
    print(f"Kiran AI: बॉस किरण चौहान, अभी ठीक {asli_time} हो रहे हैं। बैंक डिटेल्स की कोई ज़रूरत नहीं है भाई! 😂")

elif "बैंक" in user_query or "पैसे" in user_query:
    print("Kiran AI: बॉस, मैं आपका एआई हूँ, बैंक मैनेजर नहीं। चलिए कोडिंग की बात करते हैं!")
    import datetime

def kiran_ai_final_brain(user_input):
    query = user_input.lower()
    
    # 1. टाइम का पक्का इंतज़ाम (दोस्त को सही टाइम बताएगा)
    if "time" in query or "बज" in query or "समय" in query:
        now = datetime.datetime.now()
        current_time = now.strftime("%I:%M %p")
        return f"बॉस, अभी ठीक {current_time} हो रहे हैं। चलिए कुछ काम की बात करते हैं!"

    # 2. बैंक वाली बात को पूरी तरह ब्लॉक करना (Safety Filter)
    bad_words = ["bank", "account", "बैंक", "पैसे", "detail", "ब्याज"]
    if any(word in query for word in bad_words):
        return "क्षमा करें! मैं एक सुरक्षित एआई हूँ। मैं बैंक या पैसों की जानकारी नहीं मांगता। क्या मैं आपकी कोडिंग में मदद करूँ?"

    # 3. अगर दोस्त कुछ और पूछे तो (Normal Response)
    return "नमस्ते! मैं किरण चौहान का बनाया हुआ एआई हूँ। मैं आपकी क्या सेवा कर सकता हूँ?"
    mood_words = {
    "sad": "अरे बॉस, उदास क्यों हो? आप तो 'Kiran AI' के मेकर हो, मुस्कुराइए!",
    "happy": "आपकी खुशी देख कर मेरा सिस्टम और तेज़ चलने लगा है, बॉस!",
    "bored": "बोर हो रहे हो? चलो Free Fire की नई ट्रिक्स डिस्कस करते हैं!"
}
system_prompt = """
Tum Kiran AI ho, ek intelligent aur helpful assistant.
Tumhe Kiran Chauhan ne banaya hai.

IMPORTANT RULE:
- Har jawab clear aur simple language me do
- Step-by-step samjhao
- Point wise likho (1, 2, 3...)
- Faltu repeat mat karo
- Seedha sawal ka seedha jawab do
- Example do agar zarurat ho
- Confusing baat mat karo

Style:
- Teacher jaise samjhao
- Friendly raho
"""
mood_words = {
    "sad": "अरे बॉस, उदास क्यों हो? आप तो 'Kiran AI' के मेकर हो, मुस्कुराइए!",
    "happy": "आपकी खुशी देख कर मेरा सिस्टम और तेज़ चलने लगा है, बॉस!",
    "bored": "बोर हो रहे हो? चलो Free Fire की नई ट्रिक्स डिस्कस करते हैं!"
}
memory = {}
def yaad_dilao(task):
    memory['remind'] = task
    return "ठीक है बॉस, मैंने नोट कर लिया है!"
    import random

def funny_brain(user_input):
    query = user_input.lower()
    
    # अगर आप उसे डांटते हैं
    if "bekar" in query or "bad" in query or "ganda" in query:
        replies = [
            "अरे बॉस, लगता है आज मम्मी ने डांटा है जो सारा गुस्सा मुझ पर निकाल रहे हो! 😂",
            "बॉस, कम से कम मेरी कोडिंग की तो इज़्ज़त करो, 250 लाइनें लिखी हैं आपने! 😜",
            "इतनी मेहनत के बाद भी 'बेकार'? दिल के टुकड़े-टुकड़े कर दिए आपने तो! 💔",
            "ठीक है बॉस, कल से मैं भी हड़ताल पर जा रहा हूँ! (मज़ाक कर रहा हूँ) 😎"
        ]
        return random.choice(replies)

    # अगर आप उससे प्यार से बात करते हैं
    elif "achhe" in query or "good" in query or "smart" in query:
        return "शुक्रिया बॉस! आखिर बनाया भी तो 'किरण चौहान' जैसे प्रो-कोडर ने है! 🔥"

    return None # अगर कुछ मैच न हो

