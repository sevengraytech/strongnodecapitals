# TODO: Email verification hardening (OTP-only)

- [ ] Update `backend/routers/auth.py`:
  - [ ] Make `/auth/register` send OTP email (use `request-email-otp` logic internally) instead of link-token email.
  - [ ] Remove/stop using `registration_gate` flow for frontend OTP page; make UI rely on OTP endpoints.
  - [ ] Add rate limiting for `POST /auth/request-email-otp` (cooldown + cap).
  - [ ] Add attempt limiting for `POST /auth/verify-email-otp` (max attempts per OTP record).
  - [ ] Normalize error messages to reduce account enumeration.
- [ ] Update `frontend/register.html`:
  - [ ] Fix redirect URL so it no longer depends on missing `registration_gate`.
  - [ ] Optionally auto-trigger `request-email-otp` after redirect.
- [ ] Update `frontend/verify_email_otp.html`:
  - [ ] Improve UX (disable resend until cooldown handled by backend; show clear errors).
- [ ] Run quick checks:
  - [ ] Start backend (if available) / run minimal endpoint tests (curl) for OTP request + verify.
  - [ ] Manually verify email verification works end-to-end.

