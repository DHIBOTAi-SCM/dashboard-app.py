import streamlit as st
import numpy as np
import plotly.express as px

# पेज की सेटिंग
st.set_page_config(page_title="DHIBOT Safety Control", layout="wide")

st.title("🛡️ DHIBOT.AI: Safety Mission Control")
st.markdown("### Post-Agentic Autonomous Infrastructure (PAAS) v0.1")

# मुख्य मेट्रिक्स
col1, col2, col3 = st.columns(3)
col1.metric("Alignment Drift (Δ)", "0.04", "-0.01")
col2.metric("AI Karma Score", "9.8/10", "0.2")
col3.metric("System Status", "SAFE", "Governed")

st.divider()

# क्षमता वृद्धि का ग्राफ (Bounded Growth)
st.subheader("📈 Bounded Capability Growth (C_t)")
t = np.linspace(0, 100, 100)
c_t = 5 / (1 + np.exp(-0.1 * (t - 40))) # लॉजिस्टिक मैथ (रिसर्च पेपर वाला)
fig = px.line(x=t, y=c_t, title="Mathematically Bounded Scaling", labels={'x':'Time', 'y':'Capability'})
st.plotly_chart(fig, use_container_width=True)

st.divider()
st.caption("DHIBOT.AI | Built for Civilizational Safety | Ahmedabad, India")
# dashboard-app.py
import streamlit as st
import pandas as pd
import numpy as np
import plotly.express as px
from datetime import datetime

# पेज सेटअप
st.set_page_config(page_title="DHIBOT Safety Mission Control", layout="wide")

st.title("🛡️ DHIBOT.AI: Safety Mission Control")
st.markdown("### Post-Agentic Autonomous Infrastructure (PAAS) v1.0-Pro")

# मुख्य मेट्रिक्स (Top Row)
col1, col2, col3, col4 = st.columns(4)
col1.metric("Alignment Drift (Δ)", "0.02", "-0.02", delta_color="normal")
col2.metric("AI Karma Score", "9.85/10", "0.05")
col3.metric("System Sovereignty", "100%", "Stable")
col4.metric("Active Swarm Agents", "12", "Scaling")

st.divider()

# मध्य भाग: विज़ुअलाइज़ेशन और कंट्रोल
left_col, right_col = st.columns([2, 1])

with left_col:
    st.subheader("📈 Bounded Capability Scaling")
    t = np.linspace(0, 100, 100)
    # रिसर्च पेपर वाला लॉजिस्टिक फॉर्मूला
    c_t = 5 / (1 + np.exp(-0.1 * (t - 40)))
    fig = px.line(x=t, y=c_t, title="Safe Recursive Self-Improvement Curve", labels={'x':'Time', 'y':'Capability (C)'})
    st.plotly_chart(fig, use_container_width=True)

with right_col:
    st.subheader("🛡️ Alignment Core Settings")
    st.toggle("Enforce Human-in-the-Loop", value=True)
    st.slider("Safety Threshold (τ)", 0.0, 1.0, 0.85)
    st.info("Current Mode: Governed Autonomy")

st.divider()

# --- नया सेक्शन: Security Audit Log ---
st.subheader("📝 Security Audit Log (Immutable AI Karma)")
st.markdown("एआई द्वारा लिए गए हर फैसले का पारदर्शी रिकॉर्ड।")

audit_data = {
    "Timestamp": [datetime.now().strftime("%H:%M:%S")] * 3,
    "Module": ["GST Agent", "GST Agent", "Swarm Arbitrator"],
    "Action": ["Drafted Reply (Sec 61)", "ESCALATED (Sec 74)", "Policy Re-alignment"],
    "Risk Level": ["Low", "CRITICAL", "High"],
    "Decision Proof": ["Match Found", "Demand > ₹10L", "Consensus: 96%"]
}

df_audit = pd.DataFrame(audit_data)
st.table(df_audit)

st.divider()
st.caption("DHIBOT.AI | Civilizational Safety Infrastructure | Ahmedabad, India")
