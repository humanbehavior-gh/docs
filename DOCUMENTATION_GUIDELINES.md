# SDK Documentation Guidelines

This file tracks what should and shouldn't be included in the HumanBehavior SDK documentation based on our conversation and implementation status.

## ✅ **INCLUDE in Documentation**

### **Core API Methods**
- `HumanBehaviorTracker.init()` - Main initialization method
- `addUserInfo()` - User identification
- `auth()` - User authentication
- `start()` / `stop()` - Session control
- `addEvent()` - Raw event addition
- `getUserInfo()` - Get user information
- `getSessionId()` - Get current session ID
- `getCurrentUrl()` - Get current URL

### **Data Redaction**
- `redact()` - Enable data redaction
- `setRedactedFields()` - Set fields to redact
- `isRedactionActive()` - Check redaction status
- `getRedactedFields()` - Get redacted fields

### **Configuration Options**
- `redactFields` - CSS selectors for sensitive fields

### **React Integration**
- `HumanBehaviorProvider` - React context provider
- `useHumanBehavior()` - React hook
- Basic provider setup and usage

### **Core Features**
- Session recording (mouse, keyboard, scroll)
- Session persistence (30-minute window)
- User identification and properties
- Data redaction for sensitive fields
- Anti-blocking features (graceful degradation)

## ❌ **DO NOT INCLUDE in Documentation**

### **Debugging/Logging Features**
- `logLevel` configuration option
- `viewLogs()` method
- `enableConsoleTracking()` / `disableConsoleTracking()`
- Console log tracking functionality
- Any internal logging or debugging features

### **Advanced/Internal Methods**
- `trackNavigationEvent()` - Navigation tracking
- `trackPageView()` - Page view tracking
- `testConnection()` - Connection testing
- `getConnectionStatus()` - Connection status
- `isPreexistingUser()` - User status checking

### **Unimplemented Features**
- `customEvent()` - Custom event tracking (server-side not fully implemented)
- `ingestionUrl` configuration (hardcoded in SDK)

### **Server-Side Features**
- Any mention of server endpoints
- Database schema details
- Internal processing logic

## 📋 **Documentation Structure**

### **Required Sections**
1. **Quick Start** - Basic setup and initialization
2. **Installation** - Package installation methods
3. **Core API Reference** - Main tracker methods
4. **React Integration** - React hooks and provider
5. **Data Redaction** - Privacy and security features
6. **Session Management** - How sessions work

### **Optional Sections**
1. **Examples** - Real-world usage examples
2. **Error Handling** - How errors are handled
3. **Browser Compatibility** - Supported browsers

## 🎯 **Documentation Principles**

1. **User-Focused** - Only document what users need to know
2. **Implementation-Accurate** - Don't document features that aren't fully implemented
3. **Clean & Simple** - Keep examples and explanations straightforward
4. **Privacy-First** - Emphasize data redaction and privacy features
5. **No Internal Details** - Don't expose internal implementation details

## 📝 **Content Guidelines**

### **Code Examples**
- Use simple, practical examples
- Focus on common use cases
- Include error handling where appropriate
- Show both vanilla JS and React usage

### **Configuration**
- Only document user-configurable options
- Don't expose internal defaults
- Keep configuration minimal and focused

### **Error Messages**
- Don't document internal error codes
- Focus on user-friendly error handling
- Show graceful degradation examples

## 🔄 **Maintenance**

This file should be updated whenever:
- New features are added to the SDK
- Implementation status changes
- Documentation requirements evolve
- User feedback indicates needed changes

---

**Last Updated:** December 2024
**Based on:** Conversation about SDK documentation scope and implementation status 