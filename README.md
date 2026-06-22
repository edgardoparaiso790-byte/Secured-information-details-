# Secured-information-details-
gh repo create secureid-landing --public --source=. --remote=origin --push
/api/register — STR generation + user creation
/api/chat — ARIA (Claude-powered)
/api/verify-str — STR verification/domain-check for real-time confirmation → POST /registrations only if registrable: true and non-premium(http.request.uri.path in {"/api/register" "/api/verify-str"} 
and not http.request.method eq "POST")(http.request.uri.path contains "/api/" 
and not any(http.request.headers["content-type"][*] contains "application/json(http.request.uri.path eq "/api/verify-str"(http.request.uri.path eq "/api/chat" 
and not http.request.headers["user-agent"] matches "Mozilla|Chrome|Safari|Firefox")
