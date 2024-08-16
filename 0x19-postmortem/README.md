# Postmortem Report

## 403 Permission Denied Error for Backend-to-Frontend Communication

![alt text](<Ancient Aliens Guy-Backend to Frontend Communication_403 Permission Denied.png>)

### Incident report for 403 Permission Denied / Backend-to-Frontend Communication Issue

#### Summary

On August 1st, 2024, at 11:00 AM East Africa Time (EAT), the frontend of a website built using the MERN stack encountered a 403 Permission Denied error when attempting to fetch data from the backend. The issue did not occur during local development, where the backend-to-frontend communication was functioning correctly. The production environment faced this issue, causing the frontend to fail to receive necessary data from the backend.

#### Timeline

- **11:00 EAT** - Observed a 403 Permission Denied error when the frontend attempted to fetch data from the backend.
- **11:05 EAT** - Verified that the backend service was running correctly and responding to requests locally.
- **11:10 EAT** - Checked the CORS (Cross-Origin Resource Sharing) settings in the backend to ensure they allowed requests from the frontend domain.
- **11:15 EAT** - Noticed that CORS configuration in production was different from the local environment.
- **11:20 EAT** - Updated CORS settings on the backend to include the frontend's production domain.
- **11:25 EAT** - Deployed updated backend configuration and verified that CORS headers were correctly set in the response.
- **11:30 EAT** - Tested frontend-to-backend communication; observed that the 403 error persisted.
- **11:35 EAT** - Reviewed backend access control settings and authentication mechanisms to ensure they were not overly restrictive in production.
- **11:40 EAT** - Discovered that the API endpoint in the frontend was not properly configured to match the production backend URL.
- **11:45 EAT** - Corrected the API endpoint configuration in the frontend and redeployed the frontend application.
- **11:50 EAT** - Verified that the frontend successfully fetched data from the backend without encountering the 403 error.

#### Root Cause and Resolution

The 403 Permission Denied error was caused by incorrect CORS settings on the backend in the production environment. While the local environment had the appropriate CORS configuration, the production environment did not permit requests from the frontend's domain due to restrictive CORS settings. Additionally, the API endpoint configuration in the frontend was not aligned with the production backend URL, which contributed to the communication failure.

To resolve the issue, the CORS settings on the backend were updated to include the production frontend domain, and the API endpoint configuration in the frontend was corrected. This allowed the frontend to successfully communicate with the backend and fetch the necessary data.

#### Corrective and Preventive Measures

- **Verify CORS Configuration:** Ensure that CORS settings are correctly configured for all environments, including production, to allow requests from the frontend domain.
- **Consistent Environment Configuration:** Regularly synchronize and validate configuration settings across local and production environments to prevent discrepancies that may lead to issues.
- **Test in Production-Like Environment:** Implement testing environments that closely mimic production settings to catch configuration issues before deploying changes live.
- **Detailed Error Logging:** Enhance logging mechanisms to capture detailed error information, making it easier to diagnose and resolve issues promptly.
