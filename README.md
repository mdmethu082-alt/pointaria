# pointaria
Free points reward website
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>পয়েন্টারিয়া - ফ্রি পয়েন্ট</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', Arial, sans-serif; 
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh; 
            padding: 20px; 
            color: #333; 
        }
        .container {
            max-width: 500px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }
        .header {
            background: linear-gradient(90deg, #3B82F6, #10B981);
            color: white;
            padding: 25px;
            text-align: center;
        }
        .app-title { font-size: 28px; font-weight: bold; margin-bottom: 5px; }
        .user-info { padding: 20px; text-align: center; }
        .points-display { 
            font-size: 48px; 
            font-weight: bold; 
            color: #10B981; 
            margin: 15px 0; 
        }
        .user-avatar {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #3B82F6, #8B5CF6);
            border-radius: 50%;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 28px;
            font-weight: bold;
        }
        .task-card {
            background: #F9FAFB;
            margin: 20px;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #E5E7EB;
        }
        .task-header { display: flex; justify-content: space-between; margin-bottom: 15px; }
        .task-points { 
            background: #10B981; 
            color: white; 
            padding: 5px 15px; 
            border-radius: 20px; 
            font-weight: bold; 
        }
        .task-status { 
            background: #D1FAE5; 
            color: #065F46; 
            padding: 5px 12px; 
            border-radius: 20px; 
            font-weight: 600; 
            font-size: 14px; 
        }
        .task-title { 
            font-size: 20px; 
            font-weight: 600; 
            margin-bottom: 10px; 
            color: #1F2937; 
        }
        .task-desc { color: #6B7280; margin-bottom: 15px; }
        .task-btn {
            background: #3B82F6;
            color: white;
            border: none;
            width: 100%;
            padding: 15px;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            margin-top: 10px;
            transition: all 0.3s;
        }
        .task-btn:hover { background: #2563EB; }
        .task-footer {
            background: #D1FAE5;
            padding: 12px;
            border-radius: 8px;
            margin-top: 15px;
            text-align: center;
            color: #065F46;
            font-weight: 500;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #6B7280;
            font-size: 14px;
            border-top: 1px solid #E5E7EB;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="app-title">পয়েন্টারিয়া</div>
            <div>ফ্রি টাস্ক করুন, পয়েন্ট জমা করুন</div>
        </div>
        
        <div class="user-info">
            <div class="points-display" id="points">1,250</div>
            <div class="user-avatar">SH</div>
            <div style="font-weight: 500; color: #666;">শরিফুল</div>
        </div>
        
        <div style="padding: 0 20px 10px; text-align: center;">
            <h2 style="color: #1F2937;">টাস্কগুলো সম্পূর্ণ করুন, পয়েন্ট জমা করুন!</h2>
        </div>
        
        <div class="task-card">
            <div class="task-header">
                <span class="task-points">+100 পয়েন্ট</span>
                <span class="task-status">টাস্ক সম্পূর্ণ!</span>
            </div>
            <div class="task-title">টেলিগ্রাম কমিউনিটিতে যোগ দিন</div>
            <div class="task-desc">আমাদের অফিসিয়াল টেলিগ্রাম গ্রুপে জয়েন করুন</div>
            <button class="task-btn" style="background: #10B981;" disabled>
                <i class="fab fa-telegram"></i> সম্পূর্ণ হয়েছে
            </button>
            <div class="task-footer">
                <i class="fas fa-gift"></i> আপনি +১০০ বোনাস পয়েন্ট পেয়েছেন
            </div>
        </div>
        
        <div class="task-card">
            <div class="task-header">
                <span class="task-points">+50 পয়েন্ট</span>
                <span class="task-status">অপেক্ষমান</span>
            </div>
            <div class="task-title">টেলিগ্রাম অ্যাকাউন্ট ভেরিফাই করুন</div>
            <div class="task-desc">আপনার টেলিগ্রাম অ্যাকাউন্ট ভেরিফাই করুন</div>
            <button class="task-btn" onclick="completeTask()">
                <i class="fas fa-check-circle"></i> ভেরিফাই করুন
            </button>
        </div>
        
        <div class="task-card">
            <div class="task-header">
                <span class="task-points">+200 পয়েন্ট</span>
                <span class="task-status">অপেক্ষমান</span>
            </div>
            <div class="task-title">ফেসবুক পেজ লাইক করুন</div>
            <div class="task-desc">আমাদের ফেসবুক পেজটি লাইক করুন</div>
            <button class="task-btn" onclick="completeTask()">
                <i class="fab fa-facebook"></i> ফেসবুক পেজ ভিজিট করুন
            </button>
        </div>
        
        <div class="footer">
            © ২০২৩ পয়েন্টারিয়া | ফ্রি পয়েন্ট রিওয়ার্ড প্ল্যাটফর্ম<br>
            <small>ভার্সন 1.0 | https://mdmethu.github.io/pointaria</small>
        </div>
    </div>

    <script>
        let points = 1250;
        let tasksCompleted = 1;
        
        function completeTask() {
            points += 50;
            tasksCompleted++;
            
            // UI আপডেট
            document.getElementById('points').textContent = points.toLocaleString();
            
            // বাটন আপডেট
            const button = event.target;
            button.innerHTML = '<i class="fas fa-check"></i> সম্পূর্ণ হয়েছে';
            button.style.background = '#10B981';
            button.disabled = true;
            
            // টাস্ক স্ট্যাটাস আপডেট
            const taskCard = button.closest('.task-card');
            const statusSpan = taskCard.querySelector('.task-status');
            statusSpan.textContent = 'টাস্ক সম্পূর্ণ!';
            statusSpan.style.background = '#D1FAE5';
            statusSpan.style.color = '#065F46';
            
            // নোটিফিকেশন
            showNotification(`🎉 অভিনন্দন! আপনি ৫০ পয়েন্ট পেয়েছেন! মোট পয়েন্ট: ${points.toLocaleString()}`);
        }
        
        function showNotification(message) {
            const notification = document.createElement('div');
            notification.innerHTML = `
                <div style="
                    position: fixed;
                    top: 20px;
                    right: 20px;
                    background: #10B981;
                    color: white;
                    padding: 15px 25px;
                    border-radius: 10px;
                    box-shadow: 0 5px 20px rgba(0,0,0,0.2);
                    z-index: 1000;
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    font-weight: 600;
                ">
                    <i class="fas fa-check-circle"></i>
                    ${message}
                </div>
            `;
            document.body.appendChild(notification);
            setTimeout(() => notification.remove(), 3000);
        }
        
        console.log('পয়েন্টারিয়া ওয়েবসাইট 
        লাইভ! 🚀');
        console.log('GitHub: https://github.com/mdmethu/pointaria');
    </script>
</body>
</html>
/* style.css - পয়েন্টারিয়া ওয়েবসাইট */

/* বেসিক রিসেট */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* বডি স্টাইল */
body {
    font-family: 'Segoe UI', 'Arial', sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
    color: #333;
    line-height: 1.6;
}

/* কন্টেইনার */
.container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

/* হেডার */
.header {
    text-align: center;
    margin-bottom: 30px;
}

.logo {
    font-size: 36px;
    font-weight: bold;
    color: white;
    margin-bottom: 10px;
}

.subtitle {
    color: rgba(255, 255, 255, 0.9);
    font-size: 18px;
}

/* ইউজার সেকশন */
.user-section {
    background: white;
    border-radius: 15px;
    padding: 30px;
    margin-bottom: 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    text-align: center;
}

.points-display {
    font-size: 48px;
    font-weight: bold;
    color: #10B981;
    margin: 20px 0;
}

.user-avatar {
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, #3B82F6, #8B5CF6);
    border-radius: 50%;
    margin: 0 auto 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 32px;
    font-weight: bold;
}

/* টাস্ক কন্টেইনার */
.tasks-container {
    display: grid;
    gap: 20px;
}

/* টাস্ক কার্ড */
.task-card {
    background: white;
    border-radius: 15px;
    padding: 25px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);
}

.task-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.task-points {
    background: #10B981;
    color: white;
    padding: 8px 20px;
    border-radius: 20px;
    font-weight: bold;
    font-size: 16px;
}

.task-status {
    background: #D1FAE5;
    color: #065F46;
    padding: 8px 16px;
    border-radius: 20px;
    font-weight: 600;
}

.task-title {
    font-size: 22px;
    font-weight: 600;
    margin-bottom: 10px;
    color: #1F2937;
}

.task-desc {
    color: #6B7280;
    margin-bottom: 20px;
}

/* বাটন স্টাইল */
.task-btn {
    background: #3B82F6;
    color: white;
    border: none;
    padding: 15px 25px;
    border-radius: 10px;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    width: 100%;
    transition: all 0.3s;
}

.task-btn:hover {
    background: #2563EB;
    transform: translateY(-2px);
}

.task-btn.completed {
    background: #10B981;
    cursor: default;
}

/* টাস্ক ফুটার */
.task-footer {
    background: #D1FAE5;
    padding: 15px;
    border-radius: 10px;
    margin-top: 20px;
    color: #065F46;
    font-weight: 500;
    text-align: center;
}

/* ফুটার */
.footer {
    text-align: center;
    padding: 30px 0;
    color: white;
    font-size: 14px;
}

/* রেসপনসিভ ডিজাইন */
@media (max-width: 768px) {
    .container {
        padding: 15px;
    }
    
    .user-section {
        padding: 20px;
    }
    
    .points-display {
        font-size: 36px;
    }
    
    .task-card {
        padding: 20px;
    }
    
    .task-title {
        font-size: 20px;
    }
}

@media (max-width: 480px) {
    .logo {
        font-size: 28px;
    }
    
    .points-display {
        font-size: 32px;
    }
    
    .task-header {
        flex-direction: column;
        gap: 10px;
        align-items: flex-start;
    }
}
// script.js - পয়েন্টারিয়া ওয়েবসাইট

// এপ্লিকেশন কনফিগারেশন
const AppConfig = {
    appName: "পয়েন্টারিয়া",
    version: "1.0.0",
    defaultPoints: 1250,
    githubRepo: "https://github.com/mdmethu/pointaria",
    liveUrl: "https://mdmethu.github.io/pointaria"
};

// ইউজার ডেটা
let userData = {
    points: 1250,
    tasksCompleted: 1,
    streak: 7,
    username: "শরিফুল",
    avatar: "SH",
    completedTasks: ["task1"]
};

// ডকুমেন্ট রেডি হওয়ার পর
document.addEventListener('DOMContentLoaded', function() {
    console.log(`${AppConfig.appName} v${AppConfig.version} লোড হয়েছে!`);
    console.log(`GitHub: ${AppConfig.githubRepo}`);
    console.log(`Live: ${AppConfig.liveUrl}`);
    
    // UI ইনিশিয়ালাইজ
    initUI();
    
    // লোডিং মেসেজ
    showNotification(`স্বাগতম ${userData.username}! 🎉`, 'info');
});

// UI ইনিশিয়ালাইজ
function initUI() {
    updatePointsDisplay();
    updateTaskStatus();
}

// পয়েন্ট ডিসপ্লে আপডেট
function updatePointsDisplay() {
    const pointsElement = document.getElementById('points');
    if (pointsElement) {
        pointsElement.textContent = userData.points.toLocaleString();
    }
}

// টাস্ক স্ট্যাটাস আপডেট
function updateTaskStatus() {
    const taskButtons = document.querySelectorAll('.task-btn:not(.completed)');
    taskButtons.forEach(button => {
        const taskId = button.getAttribute('data-task-id');
        if (taskId && userData.completedTasks.includes(taskId)) {
            markTaskCompleted(button);
        }
    });
}

// টাস্ক কমপ্লিট ফাংশন
function completeTask(taskId = 'task2') {
    // চেক যদি ইতিমধ্যে সম্পূর্ণ করা হয়ে থাকে
    if (userData.completedTasks.includes(taskId)) {
        showNotification('আপনি ইতিমধ্যে এই টাস্কটি সম্পূর্ণ করেছেন!', 'warning');
        return;
    }
    
    // টাস্ক পয়েন্ট
    const taskPoints = getTaskPoints(taskId);
    
    // পয়েন্ট যোগ
    userData.points += taskPoints;
    userData.tasksCompleted += 1;
    userData.completedTasks.push(taskId);
    
    // UI আপডেট
    updatePointsDisplay();
    
    // বাটন আপডেট
    const button = event.target;
    markTaskCompleted(button);
    
    // নোটিফিকেশন
    showNotification(`🎉 অভিনন্দন! আপনি ${taskPoints} পয়েন্ট পেয়েছেন!`, 'success');
    
    // কনসোলে লগ
    console.log(`টাস্ক কমপ্লিট: ${taskId}, পয়েন্ট: +${taskPoints}, মোট: ${userData.points}`);
    
    // লোকাল স্টোরেজে সেভ (ঐচ্ছিক)
    saveToLocalStorage();
}

// টাস্ক পয়েন্ট ম্যাপ
function getTaskPoints(taskId) {
    const pointsMap = {
        'task1': 100,
        'task2': 50,
        'task3': 200,
        'task4': 150
    };
    return pointsMap[taskId] || 100;
}

// টাস্ক কমপ্লিটেড মার্ক
function markTaskCompleted(button) {
    button.innerHTML = '<i class="fas fa-check"></i> সম্পূর্ণ হয়েছে';
    button.classList.add('completed');
    button.disabled = true;
    
    // স্ট্যাটাস আপডেট
    const taskCard = button.closest('.task-card');
    const statusSpan = taskCard.querySelector('.task-status');
    if (statusSpan) {
        statusSpan.textContent = 'টাস্ক সম্পূর্ণ!';
        statusSpan.style.background = '#D1FAE5';
        statusSpan.style.color = '#065F46';
    }
}

// নোটিফিকেশন সিস্টেম
function showNotification(message, type = 'info') {
    // বিদ্যমান নোটিফিকেশন মুছে ফেলুন
    const existing = document.querySelector('.notification');
    if (existing) existing.remove();
    
    // আইকন ও কালার সেট
    const icons = {
        success: 'fa-check-circle',
        error: 'fa-exclamation-circle',
        warning: 'fa-exclamation-triangle',
        info: 'fa-info-circle'
    };
    
    const colors = {
        success: '#10B981',
        error: '#EF4444',
        warning: '#F59E0B',
        info: '#3B82F6'
    };
    
    // নোটিফিকেশন এলিমেন্ট তৈরি
    const notification = document.createElement('div');
    notification.className = 'notification';
    notification.innerHTML = `
        <div style="
            position: fixed;
            top: 20px;
            right: 20px;
            background: ${colors[type]};
            color: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);
            z-index: 1000;
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            max-width: 400px;
        ">
            <i class="fas ${icons[type]}"></i>
            <span>${message}</span>
        </div>
    `;
    
    document.body.appendChild(notification);
    
    // ৪ সেকেন্ড পর মুছে ফেলুন
    setTimeout(() => {
        notification.remove();
    }, 4000);
}

// লোকাল স্টোরেজ ফাংশন (ঐচ্ছিক)
function saveToLocalStorage() {
    try {
        localStorage.setItem('pointaria_user_data', JSON.stringify(userData));
    } catch (error) {
        console.log('লোকাল স্টোরেজে সেভ করতে সমস্যা:', error);
    }
}

function loadFromLocalStorage() {
    try {
        const saved = localStorage.getItem('pointaria_user_data');
        if (saved) {
            userData = JSON.parse(saved);
        }
    } catch (error) {
        console.log('লোকাল স্টোরেজ থেকে লোড করতে সমস্যা:', error);
    }
}

// গ্লোবাল এক্সপোজ
window.completeTask = completeTask;
window.showNotification = showNotification;

// শুরুতেই লোকাল স্টোরেজ থেকে লোড
loadFromLocalStorage();

console.log('Pointaria JavaScript লোড সম্পূর্ণ! 🚀');
