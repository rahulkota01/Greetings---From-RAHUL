!pip install streamlit -q

code = '''
import streamlit as st
import time

# Page setup
st.set_page_config(page_title="Greetings from RAHUL", layout="centered")

# Animated title
st.markdown("<h1 style='color:#1E90FF; text-align:center;'>Greetings---From-RAHUL</h1>", unsafe_allow_html=True)
st.markdown("<h3 style='color:#FF1493; text-align:center;'>A Page To Greet You ..... Made By RAHUL And AI&ML</h3>", unsafe_allow_html=True)

# Typewriter effect
def typewriter(text, delay=0.1):
    display = st.empty()
    full = ""
    for char in text:
        full += char
        display.markdown(f"<h4 style='text-align:center; color:#32CD32;'>{full}</h4>", unsafe_allow_html=True)
        time.sleep(delay)

typewriter("Welcome to your very own AI greeting page!")

# Fancy emoji
st.markdown("<h2 style='text-align:center;'>✨ Stay Inspired! ✨</h2>", unsafe_allow_html=True)
'''

with open("app.py", "w") as f:
    f.write(code)