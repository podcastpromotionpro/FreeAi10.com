<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MicroEarn - Support</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Poppins', sans-serif; background: #f8fafc; color: #333; }
        .container { width: 90%; max-width: 1200px; margin: 0 auto; padding: 0 15px; }
        
        /* Header */
        header { background: white; box-shadow: 0 2px 10px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 1000; }
        .header-content { display: flex; justify-content: space-between; align-items: center; padding: 15px 0; }
        .logo { display: flex; align-items: center; gap: 10px; text-decoration: none; }
        .logo-icon { background: linear-gradient(135deg, #10b981, #3b82f6); color: white; width: 40px; height: 40px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 1.5rem; }
        .logo-text { font-size: 1.8rem; font-weight: 700; background: linear-gradient(to right, #10b981, #3b82f6); -webkit-background-clip: text; background-clip: text; color: transparent; }
        
        nav ul { display: flex; list-style: none; gap: 25px; }
        nav a { color: #4b5563; text-decoration: none; font-weight: 500; transition: color 0.3s; }
        nav a:hover, nav a.active { color: #10b981; }
        
        .balance-box { background: linear-gradient(135deg, #10b981, #3b82f6); color: white; padding: 8px 15px; border-radius: 8px; font-weight: 600; }
        
        /* Page Header */
        .page-header { margin: 40px 0 30px; }
        .page-header h1 { font-size: 2.5rem; color: #111827; margin-bottom: 10px; }
        .page-header p { color: #6b7280; max-width: 600px; }
        
        /* Support Options */
        .support-options { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin-bottom: 60px; }
        .support-card { background: white; border-radius: 16px; padding: 40px; text-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.08); transition: all 0.3s; }
        .support-card:hover { transform: translateY(-5px); box-shadow: 0 15px 40px rgba(16, 185, 129, 0.15); }
        .support-icon { width: 80px; height: 80px; background: #ecfdf5; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 25px; color: #10b981; font-size: 2rem; }
        .support-card h3 { margin-bottom: 15px; color: #111827; }
        .support-card p { color: #6b7280; margin-bottom: 25px; }
        
        .btn { padding: 14px 30px; border-radius: 8px; font-weight: 600; text-decoration: none; transition: all 0.3s; cursor: pointer; border: none; font-size: 1rem; }
        .btn-primary { background: linear-gradient(to right, #10b981, #3b82f6); color: white; }
        .btn-primary:hover { transform: translateY(-3px); box-shadow: 0 10px 20px rgba(16, 185, 129, 0.3); }
        .btn-whatsapp { background: #25d366; color: white; }
        .btn-whatsapp:hover { transform: translateY(-3px); box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3); }
        .btn-livechat { background: #3b82f6; color: white; }
        .btn-livechat:hover { transform: translateY(-3px); box-shadow: 0 10px 20px rgba(59, 130, 246, 0.3); }
        
        /* Contact Form */
        .contact-form { background: white; border-radius: 16px; padding: 50px; margin-bottom: 60px; box-shadow: 0 10px 30px rgba(0,0,0,0.08); }
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 25px; margin-bottom: 25px; }
        .form-group { margin-bottom: 25px; }
        label { display: block; margin-bottom: 10px; font-weight: 500; color: #4b5563; }
        .required:after { content: " *"; color: #ef4444; }
        
        input, select, textarea { width: 100%; padding: 14px; border: 1px solid #d1d5db; border-radius: 8px; font-family: 'Poppins', sans-serif; font-size: 1rem; }
        input:focus, select:focus, textarea:focus { outline: none; border-color: #10b981; box-shadow: 0 0 0 3px rgba(16, 185, 129, 0.1); }
        textarea { min-height: 150px; resize: vertical; }
        
        /* FAQ Section */
        .faq-section { margin-bottom: 60px; }
        .faq-container { background: white; border-radius: 16px; padding: 40px; box-shadow: 0 10px 30px rgba(0,0,0,0.08); }
        .faq-item { margin-bottom: 20px; border: 1px solid #e5e7eb; border-radius: 12px; overflow: hidden; }
        .faq-question { padding: 20px; background: #f9fafb; font-weight: 600; color: #111827; cursor: pointer; display: flex; justify-content: space-between; align-items: center; }
        .faq-answer { padding: 20px; color: #6b7280; display: none; }
        .faq-item.active .faq-answer { display: block; }
        .faq-item.active .faq-question { background: #ecfdf5; color: #10b981; }
        
        /* Ticket System */
        .ticket-system { background: white; border-radius: 16px; padding: 40px; margin-bottom: 60px; box-shadow: 0 10px 30px rgba(0,0,0,0.08); }
        .ticket-list { margin-top: 30px; }
        .ticket-item { padding: 20px; border: 1px solid #e5e7eb; border-radius: 12px; margin-bottom: 15px; }
        .ticket-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px; }
        .ticket-id { font-weight: 600; color: #111827; }
        .ticket-status { padding: 5px 15px; border-radius: 20px; font-size: 0.9rem; font-weight: 600; }
        .status-open { background: #fef3c7; color: #92400e; }
        .status-closed { background: #d1fae5; color: #065f46; }
        .status-pending { background: #dbeafe; color: #1e40af; }
        .ticket-subject { font-weight: 600; color: #111827; margin-bottom: 10px; }
        .ticket-date { color: #6b7280; font-size: 0.9rem; }
        
        /* Footer */
        footer { background: #111827; color: white; padding: 60px 0 30px; margin-top: 60px; }
        .copyright { text-align: center; padding-top: 30px; border-top: 1px solid #374151; color: #9ca3af; }
        
        @media (max-width: 768px) {
            .header-content { flex-direction: column; gap: 20px; }
            nav ul { flex-wrap: wrap; justify-content: center; }
            .form-row { grid-template-columns: 1fr; }
            .support-options { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <a href="index.html" class="logo">
                    <div class="logo-icon">ME</div>
                    <div class="logo-text">MicroEarn</div>
                </a>
                
                <nav>
                    <ul>
                        <li><a href="index.html">Home</a></li>
                        <li><a href="myjobs.html">My Jobs</a></li>
                        <li><a href="packages.html">Packages</a></li>
                        <li><a href="postjob.html">Post Job</a></li>
                        <li><a href="deposit.html">Deposit</a></li>
                        <li><a href="support.html" class="active">Support</a></li>
                    </ul>
                </nav>
                
                <div class="balance-box">
                    <i class="fas fa-wallet"></i> Balance: $<span id="userBalance">0.00</span>
                </div>
            </div>
        </div>
    </header>

    <main class="container">
        <!-- Page Header -->
        <div class="page-header">
            <h1>Support Center</h1>
            <p>Get help with your account, deposits, withdrawals, and jobs. We're here to help you 24/7.</p>
        </div>
        
        <!-- Support Options -->
        <div class="support-options">
            <!-- Email Support -->
            <div class="support-card">
                <div class="support-icon">
                    <i class="fas fa-envelope"></i>
                </div>
                <h3>Email Support</h3>
                <p>Send us an email and get a response within 24 hours. Perfect for detailed inquiries.</p>
                <div style="margin: 25px 0; font-size: 1.2rem; font-weight: 600; color: #10b981;">support@microearn.com</div>
                <button class="btn btn-primary" onclick="openEmailSupport()">Send Email</button>
            </div>
            
            <!-- WhatsApp Support -->
            <div class="support-card">
                <div class="support-icon">
                    <i class="fab fa-whatsapp"></i>
                </div>
                <h3>WhatsApp Support</h3>
                <p>Chat with our support team directly on WhatsApp. Quick responses for urgent issues.</p>
                <div style="margin: 25px 0; font-size: 1.2rem; font-weight: 600; color: #25d366;">+1 (555) 123-4567</div>
                <button class="btn btn-whatsapp" onclick="openWhatsApp()">
                    <i class="fab fa-whatsapp"></i> Start Chat
                </button>
            </div>
            
            <!-- Live Chat -->
            <div class="support-card">
                <div class="support-icon">
                    <i class="fas fa-comments"></i>
                </div>
                <h3>Live Chat</h3>
                <p>Chat with us in real-time during business hours (9AM-6PM, Monday-Friday).</p>
                <div style="margin: 25px 0;">
                    <div style="background: #d1fae5; padding: 10px; border-radius: 6px; display: inline-block;">
                        Status: <span style="color: #065f46; font-weight: 600;">Online</span>
                    </div>
                </div>
                <button class="btn btn-livechat" onclick="startLiveChat()">Start Live Chat</button>
            </div>
        </div>
        
        <!-- Contact Form -->
        <div class="contact-form">
            <h2 style="margin-bottom: 30px; color: #111827;">Submit a Support Ticket</h2>
            
            <form id="supportForm">
                <div class="form-row">
                    <div class="form-group">
                        <label for="name" class="required">Your Name</label>
                        <input type="text" id="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email" class="required">Email Address</label>
                        <input type="email" id="email" required>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="subject" class="required">Subject</label>
                    <select id="subject" required>
                        <option value="">Select a topic</option>
                        <option value="deposit">Deposit Issues</option>
                        <option value="withdrawal">Withdrawal Issues</option>
                        <option value="jobs">Job Related Issues</option>
                        <option value="account">Account Issues</option>
                        <option value="verification">Verification Issues</option>
                        <option value="technical">Technical Issues</option>
                        <option value="other">Other</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="message" class="required">Message</label>
                    <textarea id="message" placeholder="Describe your issue in detail. Please include relevant information like transaction IDs, job IDs, etc." required></textarea>
                </div>
                
                <div class="form-group">
                    <label for="attachment">Attachment (Optional)</label>
                    <input type="file" id="attachment">
                    <div style="font-size: 0.9rem; color: #6b7280; margin-top: 5px;">You can attach screenshots or documents (max 5MB)</div>
                </div>
                
                <button type="submit" class="btn btn-primary" style="width: 100%;">Submit Ticket</button>
            </form>
        </div>
        
        <!-- FAQ Section -->
        <div class="faq-section">
            <h2 style="margin-bottom: 30px; color: #111827;">Frequently Asked Questions</h2>
            
            <div class="faq-container">
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        What is the minimum deposit amount?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        The minimum deposit amount is $100. This is required to start working on micro jobs. You can deposit more for additional benefits and bonuses.
                    </div>
                </div>
                
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        What is the minimum withdrawal amount?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        The minimum withdrawal amount is $300. Withdrawal fees vary by payment method: 1.5% for bKash/Nagad/Rocket, 2.5% for bank transfers.
                    </div>
                </div>
                
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        How long do deposits take to process?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        Deposits are processed within 1-2 hours during business hours. If you don't see your deposit within 24 hours, please contact support with your transaction ID.
                    </div>
                </div>
                
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        How long do withdrawals take to process?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        bKash/Nagad/Rocket withdrawals: 1-24 hours. Bank transfers: 1-3 business days. PayPal/Skrill: 1-48 hours.
                    </div>
                </div>
                
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        How do I earn from the referral program?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        You earn 40 TK for each friend who signs up using your referral link, deposits minimum $100, and completes their first job successfully.
                    </div>
                </div>
                
                <div class="faq-item" onclick="toggleFAQ(this)">
                    <div class="faq-question">
                        What if my job submission is rejected?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        If your job submission is rejected, you'll receive a reason. You can either fix the issue and resubmit or contact support if you believe it was rejected in error.
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Ticket System -->
        <div class="ticket-system">
            <h2 style="margin-bottom: 30px; color: #111827;">Your Support Tickets</h2>
            
            <div class="ticket-list" id="ticketList">
                <!-- Tickets will be loaded here -->
            </div>
            
            <div id="noTicketsMessage" style="text-align: center; padding: 40px;">
                <i class="fas fa-ticket-alt" style="font-size: 3rem; color: #d1d5db; margin-bottom: 20px;"></i>
                <h3 style="color: #6b7280; margin-bottom: 10px;">No Support Tickets</h3>
                <p style="color: #9ca3af;">You haven't submitted any support tickets yet.</p>
            </div>
        </div>
    </main>

    <!-- Live Chat Modal -->
    <div id="liveChatModal" style="display: none; position: fixed; bottom: 20px; right: 20px; width: 350px; background: white; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.2); z-index: 2000;">
        <div style="background: linear-gradient(to right, #10b981, #3b82f6); color: white; padding: 20px; border-radius: 12px 12px 0 0;">
            <div style="display: flex; justify-content: space-between; align-items: center;">
                <h3 style="margin: 0; font-size: 1.2rem;">Live Chat Support</h3>
                <button onclick="closeLiveChat()" style="background: none; border: none; color: white; font-size: 1.5rem; cursor: pointer;">&times;</button>
            </div>
            <div style="font-size: 0.9rem; opacity: 0.9; margin-top: 5px;">Typically replies within 5 minutes</div>
        </div>
        
        <div style="padding: 20px; max-height: 400px; overflow-y: auto;" id="chatMessages">
            <div style="background: #f3f4f6; padding: 12px; border-radius: 12px; margin-bottom: 15px; max-width: 80%;">
                <div style="font-weight: 600; margin-bottom: 5px;">Support Agent</div>
                <div>Hello! How can I help you today?</div>
                <div style="font-size: 0.8rem; color: #6b7280; margin-top: 5px;">Just now</div>
            </div>
        </div>
        
        <div style="padding: 20px; border-top: 1px solid #e5e7eb;">
            <div style="display: flex; gap: 10px;">
                <input type="text" id="chatInput" placeholder="Type your message..." style="flex: 1; padding: 12px; border: 1px solid #d1d5db; border-radius: 6px;">
                <button class="btn btn-primary" onclick="sendChatMessage()">Send</button>
            </div>
        </div>
    </div>

    <footer>
        <div class="container">
            <div class="copyright">
                <p>&copy; 2023 MicroEarn. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Load user balance
        document.addEventListener('DOMContentLoaded', function() {
            const savedData = localStorage.getItem('microEarnUserData');
            if (savedData) {
                const userData = JSON.parse(savedData);
                document.getElementById('userBalance').textContent = userData.balance.toFixed(2);
                
                // Pre-fill form with user data
                document.getElementById('name').value = userData.name || '';
                document.getElementById('email').value = userData.email || '';
                
                // Load tickets
                if (userData.supportTickets && userData.supportTickets.length > 0) {
                    loadTickets(userData.supportTickets);
                    document.getElementById('noTicketsMessage').style.display = 'none';
                }
            }
        });
        
        // Submit support form
        document.getElementById('supportForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            if (!name || !email || !subject || !message) {
                alert('Please fill in all required fields.');
                return;
            }
            
            // Create ticket
            const ticket = {
                id: 'TICKET-' + Date.now().toString().slice(-8),
                name: name,
                email: email,
                subject: subject,
                message: message,
                status: 'Open',
                date: new Date().toLocaleDateString('en-US'),
                timestamp: Date.now()
            };
            
            // Save to user data
            const savedData = localStorage.getItem('microEarnUserData');
            if (savedData) {
                const userData = JSON.parse(savedData);
                if (!userData.supportTickets) {
                    userData.supportTickets = [];
                }
                userData.supportTickets.unshift(ticket);
                localStorage.setItem('microEarnUserData', JSON.stringify(userData));
                
                // Update ticket list
                loadTickets(userData.supportTickets);
                document.getElementById('noTicketsMessage').style.display = 'none';
            }
            
            // Show success message
            alert(`Support ticket submitted successfully!\n\nTicket ID: ${ticket.id}\n\nWe'll respond to your ticket within 24 hours.`);
            
            // Clear form
            document.getElementById('supportForm').reset();
            document.getElementById('name').value = userData.name || '';
            document.getElementById('email').value = userData.email || '';
        });
        
        // Load tickets
        function loadTickets(tickets) {
            const ticketList = document.getElementById('ticketList');
            ticketList.innerHTML = '';
            
            // Show only last 5 tickets
            const recentTickets = tickets.slice(0, 5);
            
            recentTickets.forEach(ticket => {
                const subjectText = {
                    'deposit': 'Deposit Issues',
                    'withdrawal': 'Withdrawal Issues',
                    'jobs': 'Job Related Issues',
                    'account': 'Account Issues',
                    'verification': 'Verification Issues',
                    'technical': 'Technical Issues',
                    'other': 'Other'
                }[ticket.subject] || ticket.subject;
                
                const ticketItem = document.createElement('div');
                ticketItem.className = 'ticket-item';
                ticketItem.innerHTML = `
                    <div class="ticket-header">
                        <div class="ticket-id">${ticket.id}</div>
                        <div class="ticket-status status-${ticket.status.toLowerCase()}">${ticket.status}</div>
                    </div>
                    <div class="ticket-subject">${subjectText}</div>
                    <div style="color: #6b7280; margin-bottom: 15px;">${ticket.message.substring(0, 100)}...</div>
                    <div class="ticket-date">Submitted: ${ticket.date}</div>
                `;
                ticketList.appendChild(ticketItem);
            });
        }
        
        // Toggle FAQ
        function toggleFAQ(element) {
            element.classList.toggle('active');
        }
        
        // Support functions
        function openEmailSupport() {
            window.location.href = 'mailto:support@microearn.com';
        }
        
        function openWhatsApp() {
            const message = 'Hello, I need help with my MicroEarn account.';
            const url = `https://wa.me/15551234567?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }
        
        function startLiveChat() {
            document.getElementById('liveChatModal').style.display = 'block';
        }
        
        function closeLiveChat() {
            document.getElementById('liveChatModal').style.display = 'none';
            document.getElementById('chatInput').value = '';
        }
        
        function sendChatMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (!message) return;
            
            // Add user message
            const chatMessages = document.getElementById('chatMessages');
            const userMessage = document.createElement('div');
            userMessage.style.cssText = 'background: #10b981; color: white; padding: 12px; border-radius: 12px; margin-bottom: 15px; max-width: 80%; margin-left: auto;';
            userMessage.innerHTML = `
                <div style="font-weight: 600; margin-bottom: 5px;">You</div>
                <div>${message}</div>
                <div style="font-size: 0.8rem; opacity: 0.9; margin-top: 5px;">Just now</div>
            `;
            chatMessages.appendChild(userMessage);
            
            // Clear input
            input.value = '';
            
            // Scroll to bottom
            chatMessages.scrollTop = chatMessages.scrollHeight;
            
            // Simulate agent response after 2 seconds
            setTimeout(() => {
                const responses = [
                    "I understand. Can you please provide more details about your issue?",
                    "Thank you for sharing that information. Let me check this for you.",
                    "I'll help you resolve this issue. Please give me a moment.",
                    "Could you please share your account ID or transaction ID for reference?",
                    "I've noted your concern. Our team will look into this and get back to you soon."
                ];
                
                const randomResponse = responses[Math.floor(Math.random() * responses.length)];
                
                const agentMessage = document.createElement('div');
                agentMessage.style.cssText = 'background: #f3f4f6; padding: 12px; border-radius: 12px; margin-bottom: 15px; max-width: 80%;';
                agentMessage.innerHTML = `
                    <div style="font-weight: 600; margin-bottom: 5px;">Support Agent</div>
                    <div>${randomResponse}</div>
                    <div style="font-size: 0.8rem; color: #6b7280; margin-top: 5px;">Just now</div>
                `;
                chatMessages.appendChild(agentMessage);
                
                // Scroll to bottom
                chatMessages.scrollTop = chatMessages.scrollHeight;
            }, 2000);
        }
        
        // Close chat when clicking outside
        window.addEventListener('click', function(event) {
            const modal = document.getElementById('liveChatModal');
            if (!modal.contains(event.target) && event.target.id !== 'startLiveChatBtn') {
                modal.style.display = 'none';
            }
        });
        
        // Add sample tickets if none exist
        function addSampleTickets() {
            const savedData = localStorage.getItem('microEarnUserData');
            if (savedData) {
                const userData = JSON.parse(savedData);
                
                if (!userData.supportTickets || userData.supportTickets.length === 0) {
                    userData.supportTickets = [
                        {
                            id: 'TICKET-001',
                            name: userData.name || 'John Doe',
                            email: userData.email || 'john@example.com',
                            subject: 'deposit',
                            message: 'My deposit of $300 is not showing in my account. Transaction ID: TXN123456',
                            status: 'Closed',
                            date: 'Dec 10, 2023'
                        },
                        {
                            id: 'TICKET-002',
                            name: userData.name || 'John Doe',
                            email: userData.email || 'john@example.com',
                            subject: 'jobs',
                            message: 'Job completion not approved even though I submitted proper proof.',
                            status: 'Open',
                            date: 'Dec 15, 2023'
                        }
                    ];
                    
                    localStorage.setItem('microEarnUserData', JSON.stringify(userData));
                    
                    // Update display
                    loadTickets(userData.supportTickets);
                    document.getElementById('noTicketsMessage').style.display = 'none';
                }
            }
        }
        
        // Add sample data on page load
        document.addEventListener('DOMContentLoaded', addSampleTickets);
    </script>
</body>
</html>
