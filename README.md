# medicine-stock-tracker1
<!DOCTYPE html>
<html lang="en" class="h-full bg-slate-50">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MediVault - Secure Medicine Stock & Expiry Tracker</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: { sans: ['"Plus Jakarta Sans"', 'sans-serif'] },
                }
            }
        }
    </script>
</head>
<body class="h-full font-sans antialiased text-slate-800 flex flex-col">

    <!-- AUTHENTICATION WRAPPER -->
    <div id="auth-screen" class="hidden fixed inset-0 z-50 flex items-center justify-center bg-slate-900/60 backdrop-blur-sm p-4">
        <div class="bg-white rounded-2xl shadow-2xl w-full max-w-md overflow-hidden border border-slate-100">
            <div class="bg-gradient-to-r from-teal-600 to-emerald-600 p-6 text-white text-center">
                <div class="w-14 h-14 bg-white/10 rounded-2xl flex items-center justify-center mx-auto mb-3 backdrop-blur-md">
                    <i class="fa-solid fa-vault text-2xl text-white"></i>
                </div>
                <h2 id="auth-title" class="text-2xl font-bold">Welcome to MediVault</h2>
                <p id="auth-subtitle" class="text-teal-100 text-sm mt-1">Secure medicine stock & expiry tracking</p>
            </div>
            
            <form id="auth-form" class="p-6 space-y-4">
                <div id="auth-error" class="hidden p-3 bg-rose-50 border border-rose-200 text-rose-700 text-sm rounded-xl"></div>
                
                <div>
                    <label class="block text-xs font-semibold text-slate-600 uppercase tracking-wider mb-1">Email Address</label>
                    <div class="relative">
                        <span class="absolute inset-y-0 left-0 pl
