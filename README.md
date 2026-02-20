# Laptop Request Catalog Item - ServiceNow

## Overview
This project provides a ServiceNow Service Catalog Item that enables employees to request laptops in a streamlined, user-friendly, and dynamic way. It replaces outdated manual processes with a modern, automated solution that ensures accurate data collection and improved user experience.

## Features
- Dynamic form behavior using Catalog UI Policies
- Reset form functionality using a client-side UI Action
- Clear, guided form instructions for users
- Exportable update set for deployment to other ServiceNow instances
- Fully tested in a separate instance to ensure smooth deployment

## Variables Included
- Laptop Model
- Justification
- Additional Accessories (checkbox/dropdown)
- Accessories Details (shown conditionally)

## Dynamic Form Behavior
Implemented using Catalog UI Policies:
- Show/Hide `Accessories Details` field based on selection of `Additional Accessories`
- Set `Accessories Details` as mandatory if `Additional Accessories` is selected

## Reset Form Functionality
A client-side UI Action is included to allow users to reset the form.

**UI Action Details:**
- **Table**: `sc_cart`
- **Action Name**: Reset Form
- **Order**: 100
- **Client**: Checked
- **Script**:
```javascript
function resetForm() {
  g_form.clearForm(); // Clears all fields in the form
  alert("The form has been reset.");
}
```

## Conclusion

The **Laptop Request Catalog Item** streamlines the hardware request workflow in ServiceNow by replacing manual processes with an automated and structured solution. Dynamic UI policies ensure relevant fields are displayed only when necessary, improving accuracy and reducing user errors. The client-side reset functionality enhances usability by allowing quick form clearing and resubmission.

Overall, this implementation improves employee experience, reduces IT administrative overhead, and provides a scalable, maintainable, and efficient approach to laptop provisioning within the organization.
