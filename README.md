# Frontend Developer Take-Home Assignment

## Overview
Build a **Health Metrics Dashboard** that displays lab results for patients over time. This assignment focuses on frontend development skills while requiring a simple backend implementation.

**Duration**: 2 weeks  
**Theme**: Medical/Healthcare  
**Time Investment**: We estimate this assignment will take 20-25 hours over 2 weeks. We respect your time and have designed this to be a meaningful portfolio piece.

> **Repository Visibility**: Please keep your repository private during the evaluation process. To allow us to evauluate your work, please add `admin@orthonyx.com` as a collaborator/member in your private repository. After your interview is complete, you're welcome to make it public and showcase it as part of your portfolio.

> **Our Commitment**: We commit to reviewing your submission within 5 business days. Focus on demonstrating your skills rather than perfection - a well-implemented core feature set is better than rushed bonus features.

## Project Requirements

### Core Features
1. **User Authentication**
   - Sign up with email/password
   - Sign in and receive API key
   - API key authentication for all requests
   - Secure API key storage in frontend (not hardcoded)

2. **Lab Results Dashboard**
   - Display three types of lab metrics:
     - Blood Sugar (Glucose) - mg/dL
     - Cholesterol (Total, LDL, HDL) - mg/dL
     - Blood Pressure (Systolic/Diastolic) - mmHg
   - Visualize data with charts (your choice of chart types)
   - Handle irregular time intervals between lab tests
   - Mobile responsive design

3. **Data Management**
   - Add new lab results
   - View historical data
   - Generate your own realistic mock data

### Technical Stack

#### Frontend (Required)
- React
- Vite
- Tailwind CSS
- TypeScript

#### Backend (Required)
- Any language/framework you're comfortable with
- Must implement JWT authentication
- RESTful API design

#### Database (Required)
- Any database system
- Design your own schema

### API Endpoints (Minimum Required)
- `POST /auth/signup` - User registration (returns API key)
- `POST /auth/signin` - User login (returns API key)
- `GET /lab-results` - Get user's lab results (requires API key)
- `POST /lab-results` - Add new lab result (requires API key)
- `GET /user/profile` - Get user profile (requires API key)

### Data Format Example
```json
{
  "labResult": {
    "id": "uuid",
    "userId": "uuid", 
    "date": "2024-01-15",
    "results": {
      "glucose": 95,
      "cholesterol": {
        "total": 160,
        "ldl": 100,
        "hdl": 60
      },
      "bloodPressure": {
        "systolic": 120,
        "diastolic": 80
      }
    }
  }
}
```

### API Key Requirements
- All users receive the same API key (to keep backend simple for frontend-focused assignment)
- API key must be obtained through successful login (cannot be hardcoded in frontend)
- API key must be sent in Authorization header or as query parameter
- API key must be stored securely in frontend (not hardcoded in source code)
- All API requests must include valid API key or return 401 Unauthorized

## Key Challenges
- **Irregular Time Intervals**: Lab tests aren't taken at regular intervals. How will you visualize this data effectively?
- **Data Visualization**: Choose appropriate chart types for different metrics
- **State Management**: Handle authentication state and data fetching efficiently
- **User Experience**: Create an intuitive interface for viewing health data

## Evaluation Criteria

### Code Quality
- Clean, maintainable code
- TypeScript usage
- Component structure
- Error handling

### UI/UX Design
- Visual design and layout
- Mobile responsiveness
- Intuitive navigation
- Loading states and error feedback

### Frontend Architecture
- State management approach
- Component reusability
- Performance optimization
- Security best practices

### Functionality
- All features working correctly
- Edge cases handled
- Data validation
- Smooth user experience


### Documentation
- Clear README with setup instructions
- Code comments where necessary

### Bonus Points (Optional)
We recommend choosing ONE bonus feature that interests you most or aligns with your experience, and implementing it well. Quality over quantity!
- Integration tests for critical user flows
- Dark mode toggle
- Data export functionality (CSV download)
- Basic date filtering (last week, month, year)
- Loading animations and transitions
- Enhanced responsive design features

## FAQ

**Q: Can I use additional libraries?**  
A: Yes, but be prepared to justify your choices.

**Q: Can I use component libraries like Radix UI or shadcn/ui?**  
A: Absolutely! You're welcome to use any component libraries as long as you're using TailwindCSS, React, and TypeScript as the core stack.

**Q: Can I use AI/LLM tools like ChatGPT or Claude?**  
A: Yes, you may use LLM tools to help with your development. However, you must take full ownership of all code submitted, ensure its quality, and be able to explain every part of your implementation during the interview.

**Q: Do I need to write tests?**  
A: Testing is optional and listed as bonus points. Focus on delivering working features first. If you do write tests, you can use either Jest or Vitest.

**Q: How much mock data should I generate?**  
A: Enough to demonstrate your visualization approach - at least 8-12 data points per user with varying time gaps. If you're not familiar with realistic ranges for glucose, cholesterol, or blood pressure values, feel free to use LLM tools to help generate medically realistic mock data.

**Q: Should I implement user roles?**  
A: Not required. Focus on the core features.

**Q: Do I need to deploy the application?**  
A: No, local development is sufficient.

**Q: Should I optimize the backend for performance and/or security?**  
A: No, keep the backend simple. This is a frontend-focused assignment - basic CRUD operations and authentication are sufficient.

**Q: Why do I need to build a backend for a frontend assignment?**  
A: Modern frontend developers are expected to understand full-stack development and API integration. This tests your ability to design APIs that work well with your frontend and handle complete data flows.

**Q: Should I implement optional/bonus features?**  
A: Only if time permits after completing all core functionality well. A well-implemented core assignment is much better than mediocre core functionality with optional features. Focus on quality over quantity.

## Notes
- This is an open-ended assignment - feel free to showcase your creativity
- Focus on code quality over feature quantity
- If you make assumptions, document them
- Have fun and show us what you can build!

## Submission Checklist

### Core Requirements
- [ ] User authentication (signup/signin) working
- [ ] JWT token management
- [ ] Lab results dashboard displaying all three metrics
- [ ] Data visualization with appropriate charts
- [ ] Add new lab result functionality
- [ ] Mobile responsive design
- [ ] Generated realistic mock data with irregular time intervals

### Technical Requirements
- [ ] React + Vite + Tailwind CSS + TypeScript frontend
- [ ] Backend API with all required endpoints
- [ ] Database integration
- [ ] Proper error handling throughout
- [ ] Loading states for async operations
- [ ] Secure token storage implementation

### Documentation
- [ ] README with clear setup instructions and assumptions made

### Code Quality
- [ ] Clean, well-organized code structure
- [ ] TypeScript types properly defined
- [ ] Components are reusable where appropriate
- [ ] No console errors

### Final Steps
- [ ] Project runs locally without errors
- [ ] All features tested and working
- [ ] Repository pushed to GitHub/GitLab
- [ ] `admin@orthonyx.com` is added as a member in the GitHub/GitLab repository
- [ ] Verified setup instructions work on a clean install

---
*Please reach out to us via email (admin@orthonyx.com) if you have any questions about the assignment.*