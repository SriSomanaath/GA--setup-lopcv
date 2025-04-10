# 📊 Google Analytics 4 (GA4) Data API Setup via Service Account

This guide walks you through the complete process of accessing GA4 data using Google Analytics Data API v1 with a service account.

---

## 🔧 Step 1: Enable the Analytics Data API

1. Go to the [Google Cloud Console API Library](https://console.cloud.google.com/apis/library/analyticsdata.googleapis.com)
2. Choose or create your **Google Cloud project**.
3. Click **“Enable”** on the **Google Analytics Data API v1** page.

---

## 👤 Step 2: Create a Service Account

1. Go to [Service Accounts in Google Cloud Console](https://console.cloud.google.com/iam-admin/serviceaccounts)
2. Click **“+ CREATE SERVICE ACCOUNT”**
3. Fill in:
   - **Service account name**: `ga4-data-access`
   - **Description**: `Access GA4 via Data API`
4. Click **Create and Continue**
5. Skip assigning roles for now
6. Click **Done**

---

## 🔐 Step 3: Generate a Service Account Key (JSON)

1. Open the newly created service account
2. Go to the **“KEYS”** tab
3. Click **“Add Key” → “Create new key”**
4. Choose **JSON**, then click **Create**
5. Save the downloaded `.json` file securely

---

## 🔗 Step 4: Grant Access to GA4 Property

1. Go to [Google Analytics](https://analytics.google.com)
2. Open your GA4 property
3. Navigate to:
   - **Admin → Property Settings → Access Management**
4. Click **“+” → Add users**
5. Paste the **service account email**
6. Assign **Viewer** role
7. Click **Add**

---

## 📥 Step 5: Access GA4 Data via API

You can now access GA4 data using any backend language (Node.js, Python, etc.) by authenticating with your service account's JSON key.

> Want sample code in Node.js or Python? Ask ChatGPT with your preferred stack.

---

## ✅ Final Checklist

| Step                         | Done |
|------------------------------|------|
| Enabled Analytics Data API   | ✅    |
| Created Service Account      | ✅    |
| Downloaded JSON Key          | ✅    |
| Added GA4 Property Access    | ✅    |

---

## 🧠 Notes

- Service Account emails usually look like:  
  `ga4-data-access@your-project-id.iam.gserviceaccount.com`
- Only GA4 properties are supported (not Universal Analytics).
- Always store your `.json` key in `.gitignore`-ed locations for security.

---

## 💬 Need Help?

Ask ChatGPT for:
- Working code samples in Node.js, Python, or Java
- Debugging help for GA4 data queries
- Data visualization techniques using the results

---
