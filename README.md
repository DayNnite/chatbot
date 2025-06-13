📦 Widget Gateway This project hosts a gateway script that loads a third-party widget (testmyprompt.com/widget.js) through your own domain.

🚀 How It Works Clients embed your hosted gateway.js script on their website.

gateway.js automatically loads the real widget for them.

You stay in control and can update or block access in the future if needed.

📄 Embed Snippet for Clients html Copy code

<script src="https://your-app-name.onrender.com/gateway.js"></script>
✅ Replace your-app-name with your actual Render subdomain.

📂 Project Structure Copy code /gateway.js <-- The gateway loader script No backend or server is needed — this is a static hosting setup.

✨ Future Improvements Add access control (client ID, token checks)

Build a management dashboard for clients

Switch to self-hosting the widget if necessary

🛠️ Deployment Hosting: Render.com

Source Control: GitHub

Auto-deploys when pushing updates to the main branch.

📢 License Distributed for educational and business use. Widget ownership remains with the original SaaS provider (testmyprompt.com).

🙌 Credits Made with ❤️ to simplify widget distribution.
