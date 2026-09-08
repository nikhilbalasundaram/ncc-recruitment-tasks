# Newton School Coding Club - NCC Recruitment Tasks

This repository contains solutions for the **Technical Domain Recruitment Tasks** for 1st Year at Newton School Coding Club, SRM IST.

## 📋 Tasks Completed

### **Task 1: Signup Form with Validation and Dashboard**
- Build a web application for user signup, validation, and dashboard view
- Submit Link: https://forms.gle/6JBrPJCsQPzWjWKy6

### **Task 2: Personal Introduction Page**
- Build a responsive personal introduction webpage showcasing skills and personality
- Submit Link: https://forms.gle/6JBrPJCsQPzWjWKy6

---

## 🚀 How to Run the Projects

### **Task 1: Signup Form**

1. **Download the file**: `task1_signup.html`
2. **Open in browser**: 
   - Double-click the file, OR
   - Right-click → Open with → Browser
3. **No server required**: This is a standalone HTML file that runs directly in your browser

**Features**:
- ✅ Signup form with three input fields (Username, Email, Password)
- ✅ Real-time input validation using regex for email
- ✅ Password hashing before storing
- ✅ localStorage integration to persist user data
- ✅ Dashboard view with all registered users in a table
- ✅ Delete button for individual user entries (Brownie Subtask)
- ✅ Clear All Data button for bulk deletion
- ✅ Responsive design for mobile and desktop
- ✅ Beautiful gradient UI with smooth animations

### **Task 2: Personal Introduction Page**

1. **Download the file**: `task2_personal_intro.html`
2. **Open in browser**:
   - Double-click the file, OR
   - Right-click → Open with → Browser
3. **No server required**: This is a standalone HTML file

**Features**:
- ✅ Responsive design for desktop, tablet, and mobile
- ✅ Profile photo display area
- ✅ Name, introduction, and bio section
- ✅ Skills showcase with gradient cards
- ✅ Interests/Hobbies section with animated badges
- ✅ About me section with statistics
- ✅ Social media links (GitHub, LinkedIn, Twitter, Email)
- ✅ **Dark/Light Mode toggle** (Brownie Subtask) with localStorage persistence
- ✅ Smooth animations and transitions
- ✅ Beautiful gradient UI with interactive elements
- ✅ Icon support via Font Awesome CDN

---

## 🎯 Features Implemented

### **Task 1: Advanced Features**

```
Core Requirements:
├── Username validation (cannot be empty, min 3 chars)
├── Email validation (regex pattern: user@domain.ext)
├── Password validation (min 6 characters)
├── Password hashing (simple hash function implemented)
├── localStorage integration
├── Dashboard table display
├── User entry deletion
└── Clear all data functionality

UI/UX Enhancements:
├── Real-time error messages
├── Success notification
├── Toggle between Signup and Dashboard views
├── Responsive design
├── Gradient color scheme
├── Smooth animations
└── Form validation feedback
```

### **Task 2: Advanced Features**

```
Core Requirements:
├── Name and introduction display
├── Profile photo area
├── Skills showcase
├── Interests/hobbies section
├── Social media links
├── Fully responsive design
├── Clean and attractive UI
└── Interactive elements

Brownie Subtask (Dark Mode):
├── Dark/Light mode toggle button
├── localStorage persistence
├── Smooth theme transitions
└── Icon changes based on theme

Bonus Enhancements:
├── Smooth scroll animations
├── Hover effects on all interactive elements
├── Grid-based responsive layouts
├── About section with statistics
├── Intersection Observer for scroll animations
├── Font Awesome icon integration
└── CSS variables for theme management
```

---

## 💻 Technologies Used

### **Task 1**
- **HTML5**: Semantic structure
- **CSS3**: Styling with gradients, animations, media queries
- **JavaScript (ES6+)**:
  - Form validation
  - Password hashing (SHA-like simple hash)
  - localStorage API
  - DOM manipulation
  - Event listeners

### **Task 2**
- **HTML5**: Semantic structure with accessibility
- **CSS3**: 
  - CSS Grid and Flexbox
  - CSS variables for theming
  - Media queries for responsiveness
  - Keyframe animations
  - Gradients and shadows
- **JavaScript (ES6+)**:
  - localStorage for theme persistence
  - Intersection Observer API
  - Event handling

### **External Resources**
- Font Awesome 6.4.0 (CDN) - for icons
- Placeholder Image Service - for profile photos

---

## 📝 Code Explanation

### **Task 1: Key Functions**

#### **Validation Functions**
```javascript
// Email regex validation
const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

// Username validation
function validateUsername(username) {
    if (username.trim() === '') {
        return { valid: false, error: 'Username cannot be empty' };
    }
    if (username.length < 3) {
        return { valid: false, error: 'Username must be at least 3 characters' };
    }
    return { valid: true };
}

// Password hashing (simple implementation)
function simpleHash(str) {
    let hash = 0;
    for (let i = 0; i < str.length; i++) {
        const char = str.charCodeAt(i);
        hash = ((hash << 5) - hash) + char;
    }
    return 'HASH_' + Math.abs(hash).toString(16);
}
```

#### **localStorage Operations**
```javascript
// Save user
const users = JSON.parse(localStorage.getItem('users')) || [];
users.push(newUser);
localStorage.setItem('users', JSON.stringify(users));

// Load users
const users = JSON.parse(localStorage.getItem('users')) || [];

// Delete user
users = users.filter(user => user.id !== userId);
localStorage.setItem('users', JSON.stringify(users));
```

### **Task 2: Key Functions**

#### **Dark Mode Toggle**
```javascript
const themeToggle = document.getElementById('themeToggle');

// Load saved theme
const savedTheme = localStorage.getItem('theme') || 'light';
if (savedTheme === 'dark') {
    document.body.classList.add('dark-mode');
}

// Toggle theme
themeToggle.addEventListener('click', function () {
    const isDarkMode = document.body.classList.toggle('dark-mode');
    localStorage.setItem('theme', isDarkMode ? 'dark' : 'light');
});
```

#### **Intersection Observer for Animations**
```javascript
const observer = new IntersectionObserver(function (entries) {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
        }
    });
}, observerOptions);

document.querySelectorAll('.section, .hero').forEach(el => {
    observer.observe(el);
});
```

---

## 🎨 Design Highlights

### **Color Scheme**
- **Primary**: #667eea (Purple Blue)
- **Secondary**: #764ba2 (Purple)
- **Dark Mode**: Inverted backgrounds with light text

### **Responsive Breakpoints**
- **Desktop**: Full width with multi-column layouts
- **Tablet (768px)**: Adjusted grid and font sizes
- **Mobile (480px)**: Single column layouts, optimized touch targets

### **Animations**
- Slide-in animations on page load
- Hover effects on interactive elements
- Smooth transitions between theme changes
- Scale and rotate animations on buttons

---

## 📊 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## 🔒 Security Notes

**Important**: The password hashing in Task 1 is a simple demonstration and **NOT suitable for production use**. For real applications, use:
- bcrypt
- Argon2
- PBKDF2
- Server-side hashing with proper salt

The current implementation is for educational purposes to demonstrate the concept.

---

## 📚 Concepts Learned

### **Task 1**
1. **Form Validation**: Regex patterns, input validation, error handling
2. **Data Persistence**: localStorage API, JSON serialization
3. **DOM Manipulation**: Creating/removing elements dynamically
4. **Event Handling**: Form submission, click events
5. **Password Security**: Hashing concepts (basic demonstration)
6. **Responsive Design**: Media queries, flexible layouts

### **Task 2**
1. **CSS Grid & Flexbox**: Modern layout techniques
2. **CSS Variables**: Theme management and customization
3. **Responsive Design**: Mobile-first approach, media queries
4. **Animations**: Keyframes, transitions, transform effects
5. **localStorage**: Theme persistence
6. **Intersection Observer**: Scroll-based animations
7. **Accessibility**: Semantic HTML, ARIA labels

---

## 🎯 Submission Checklist

- [x] Complete source code
- [x] Well-written README (this file)
- [x] Features implementation
- [x] Responsive design
- [x] Code comments and explanation
- [x] Browser compatibility tested
- [x] All validation working
- [x] Dark mode (Task 2 Brownie Subtask)
- [x] Delete functionality (Task 1 Brownie Subtask)

---

## 👨‍💻 Developer Notes

### **What I Learned**

1. **Validation Best Practices**: Understanding regex patterns, multiple validation layers
2. **Data Management**: localStorage limitations, JSON handling, array manipulation
3. **User Experience**: Error messages, success feedback, smooth animations
4. **Responsive Web Design**: Mobile-first approach, flexibility in layouts
5. **Modern JavaScript**: ES6 features, arrow functions, destructuring
6. **CSS Mastery**: Custom properties, gradients, animations, media queries
7. **Accessibility**: Semantic HTML, proper form labels, contrast ratios

### **Challenges Overcome**

- **Password Hashing**: Implemented a simple hash function to demonstrate the concept
- **Responsive Layouts**: Used CSS Grid and Flexbox for flexible, mobile-friendly designs
- **Dark Mode**: Used CSS variables for seamless theme switching with localStorage
- **Real-time Validation**: Provided instant feedback without form submission

### **Future Enhancements**

1. Backend integration with Node.js/Express
2. Database storage (MongoDB/PostgreSQL)
3. User authentication with JWT
4. Email verification
5. Password reset functionality
6. Profile image upload
7. Blog or project portfolio section
8. Comment/feedback system

---

## 📞 Contact & Submission

- **Email**: nscc@srmist.edu.in
- **Phone**: +91 8603405145, +91 7275587001
- **Address**: SRM University, Potheri SRM Nagar, Kattankulathur, Tamil Nadu 603203

---

## 📄 License

This project is created for Newton School Coding Club recruitment purposes.

---

## 🙏 Acknowledgments

- Newton School Coding Club for the recruitment opportunity
- SRM IST for the amazing platform
- Font Awesome for icon library
- Modern CSS and JavaScript communities for inspiration

---

**Created with ❤️ for NCC Recruitment - Task 1 & 2**
