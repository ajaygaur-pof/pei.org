# pei.org
milk
[deepseek_html_20251104_eb0cac.html](https://github.com/user-attachments/files/23333608/deepseek_html_20251104_eb0cac.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Country Delight - Milk Delivery Admin</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* GitHub Style Dark Theme */
        :root {
            --github-dark: #0d1117;
            --github-dark-secondary: #161b22;
            --github-border: #30363d;
            --github-text: #c9d1d9;
            --github-blue: #58a6ff;
            --github-green: #3fb950;
            --github-orange: #ffa657;
            --github-red: #f85149;
            --github-purple: #bc8cff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
        }
        
        body {
            background-color: var(--github-dark);
            color: var(--github-text);
            line-height: 1.5;
            overflow-x: hidden;
        }
        
        .container {
            display: flex;
            min-height: 100vh;
        }
        
        /* Sidebar Styles */
        .sidebar {
            width: 280px;
            background-color: var(--github-dark-secondary);
            border-right: 1px solid var(--github-border);
            display: flex;
            flex-direction: column;
            transition: all 0.3s ease;
        }
        
        .sidebar-header {
            padding: 20px;
            border-bottom: 1px solid var(--github-border);
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .sidebar-header h2 {
            font-size: 20px;
            font-weight: 600;
            background: linear-gradient(135deg, var(--github-green), var(--github-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .logo {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--github-green), var(--github-blue));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
        }
        
        .nav-section {
            padding: 20px 0;
            border-bottom: 1px solid var(--github-border);
        }
        
        .nav-title {
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
            padding: 8px 20px;
            color: #8b949e;
            letter-spacing: 0.5px;
        }
        
        .nav-item {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 20px;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 14px;
            border-left: 3px solid transparent;
        }
        
        .nav-item:hover {
            background-color: rgba(255, 255, 255, 0.05);
        }
        
        .nav-item.active {
            background-color: rgba(88, 166, 255, 0.1);
            font-weight: 600;
            border-left-color: var(--github-blue);
            color: var(--github-blue);
        }
        
        .nav-item i {
            width: 18px;
            text-align: center;
            font-size: 16px;
        }
        
        /* Main Content Styles */
        .main-content {
            flex: 1;
            display: flex;
            flex-direction: column;
            background: var(--github-dark);
        }
        
        .header {
            padding: 20px 32px;
            background-color: var(--github-dark-secondary);
            border-bottom: 1px solid var(--github-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
            backdrop-filter: blur(10px);
        }
        
        .header-title {
            font-size: 24px;
            font-weight: 700;
        }
        
        .header-actions {
            display: flex;
            gap: 16px;
            align-items: center;
        }
        
        .search-box {
            background-color: var(--github-dark);
            border: 1px solid var(--github-border);
            border-radius: 8px;
            padding: 10px 16px;
            color: var(--github-text);
            font-size: 14px;
            width: 300px;
            transition: all 0.2s ease;
        }
        
        .search-box:focus {
            outline: none;
            border-color: var(--github-blue);
            box-shadow: 0 0 0 3px rgba(88, 166, 255, 0.1);
        }
        
        .btn {
            background-color: var(--github-dark-secondary);
            border: 1px solid var(--github-border);
            color: var(--github-text);
            padding: 10px 20px;
            border-radius: 8px;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 500;
        }
        
        .btn:hover {
            background-color: rgba(255, 255, 255, 0.05);
            border-color: var(--github-blue);
            transform: translateY(-1px);
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--github-green), var(--github-blue));
            border: none;
            color: white;
            font-weight: 600;
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(63, 185, 80, 0.3);
        }
        
        .content {
            flex: 1;
            padding: 32px;
            overflow-y: auto;
        }
        
        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 24px;
            margin-bottom: 32px;
        }
        
        .stat-card {
            background: var(--github-dark-secondary);
            border: 1px solid var(--github-border);
            border-radius: 12px;
            padding: 24px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--github-green), var(--github-blue));
        }
        
        .stat-card:hover {
            transform: translateY(-4px);
            border-color: var(--github-blue);
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
        }
        
        .stat-title {
            font-size: 14px;
            color: #8b949e;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 500;
        }
        
        .stat-value {
            font-size: 32px;
            font-weight: 700;
            margin-bottom: 8px;
            background: linear-gradient(135deg, var(--github-text), var(--github-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-change {
            font-size: 13px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 4px;
        }
        
        .positive {
            color: var(--github-green);
        }
        
        .negative {
            color: var(--github-red);
        }
        
        /* Tabs */
        .tabs {
            display: flex;
            border-bottom: 1px solid var(--github-border);
            margin-bottom: 24px;
            gap: 4px;
        }
        
        .tab {
            padding: 12px 24px;
            cursor: pointer;
            font-size: 14px;
            border-bottom: 2px solid transparent;
            transition: all 0.2s ease;
            font-weight: 500;
            border-radius: 6px 6px 0 0;
        }
        
        .tab:hover {
            background-color: rgba(255, 255, 255, 0.03);
        }
        
        .tab.active {
            border-bottom-color: var(--github-orange);
            color: var(--github-orange);
            background-color: rgba(255, 166, 87, 0.05);
        }
        
        /* Cards */
        .card {
            background: var(--github-dark-secondary);
            border: 1px solid var(--github-border);
            border-radius: 12px;
            margin-bottom: 24px;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .card:hover {
            border-color: var(--github-blue);
        }
        
        .card-header {
            padding: 20px 24px;
            border-bottom: 1px solid var(--github-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(255, 255, 255, 0.02);
        }
        
        .card-title {
            font-size: 18px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card-body {
            padding: 24px;
        }
        
        /* Tables */
        .table {
            width: 100%;
            border-collapse: collapse;
            font-size: 14px;
        }
        
        .table th {
            text-align: left;
            padding: 16px;
            border-bottom: 1px solid var(--github-border);
            font-weight: 600;
            color: #8b949e;
            background: rgba(255, 255, 255, 0.02);
        }
        
        .table td {
            padding: 16px;
            border-bottom: 1px solid var(--github-border);
        }
        
        .table tr:last-child td {
            border-bottom: none;
        }
        
        .table tr:hover {
            background-color: rgba(255, 255, 255, 0.03);
        }
        
        /* Badges */
        .badge {
            display: inline-block;
            padding: 6px 12px;
            font-size: 12px;
            font-weight: 600;
            border-radius: 20px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .badge-success {
            background: rgba(63, 185, 80, 0.15);
            color: var(--github-green);
            border: 1px solid rgba(63, 185, 80, 0.3);
        }
        
        .badge-warning {
            background: rgba(255, 166, 87, 0.15);
            color: var(--github-orange);
            border: 1px solid rgba(255, 166, 87, 0.3);
        }
        
        .badge-danger {
            background: rgba(248, 81, 73, 0.15);
            color: var(--github-red);
            border: 1px solid rgba(248, 81, 73, 0.3);
        }
        
        .badge-info {
            background: rgba(88, 166, 255, 0.15);
            color: var(--github-blue);
            border: 1px solid rgba(88, 166, 255, 0.3);
        }
        
        /* Customer Avatar */
        .customer-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--github-purple), var(--github-blue));
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            font-size: 14px;
            color: white;
        }
        
        .customer-info {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .customer-details {
            display: flex;
            flex-direction: column;
        }
        
        .customer-name {
            font-weight: 600;
        }
        
        .customer-id {
            font-size: 12px;
            color: #8b949e;
        }
        
        /* Action Buttons */
        .action-btns {
            display: flex;
            gap: 8px;
        }
        
        .action-btn {
            background: none;
            border: 1px solid var(--github-border);
            color: var(--github-text);
            cursor: pointer;
            padding: 8px;
            border-radius: 6px;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .action-btn:hover {
            background-color: rgba(255, 255, 255, 0.05);
            border-color: var(--github-blue);
            color: var(--github-blue);
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(5px);
        }
        
        .modal-content {
            background-color: var(--github-dark-secondary);
            border: 1px solid var(--github-border);
            border-radius: 12px;
            width: 500px;
            max-width: 90vw;
            max-height: 90vh;
            overflow-y: auto;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
        }
        
        .modal-header {
            padding: 24px;
            border-bottom: 1px solid var(--github-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .modal-title {
            font-size: 20px;
            font-weight: 600;
        }
        
        .modal-close {
            background: none;
            border: none;
            color: var(--github-text);
            font-size: 20px;
            cursor: pointer;
            padding: 4px;
            border-radius: 4px;
            transition: all 0.2s ease;
        }
        
        .modal-close:hover {
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--github-red);
        }
        
        .modal-body {
            padding: 24px;
        }
        
        .modal-footer {
            padding: 24px;
            border-top: 1px solid var(--github-border);
            display: flex;
            justify-content: flex-end;
            gap: 12px;
        }
        
        /* Form Elements */
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-label {
            display: block;
            margin-bottom: 8px;
            font-size: 14px;
            font-weight: 500;
            color: #8b949e;
        }
        
        .form-control {
            width: 100%;
            background-color: var(--github-dark);
            border: 1px solid var(--github-border);
            border-radius: 8px;
            padding: 12px 16px;
            color: var(--github-text);
            font-size: 14px;
            transition: all 0.2s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--github-blue);
            box-shadow: 0 0 0 3px rgba(88, 166, 255, 0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 1024px) {
            .container {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                height: auto;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .header {
                padding: 16px 20px;
            }
            
            .content {
                padding: 20px;
            }
            
            .search-box {
                width: 200px;
            }
        }
        
        @media (max-width: 768px) {
            .header-actions {
                flex-direction: column;
                gap: 12px;
                width: 100%;
            }
            
            .search-box {
                width: 100%;
            }
            
            .table {
                font-size: 12px;
            }
            
            .table th,
            .table td {
                padding: 12px 8px;
            }
        }
        
        /* Loading Animation */
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--github-blue);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: var(--github-dark);
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--github-border);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--github-blue);
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Sidebar -->
        <div class="sidebar">
            <div class="sidebar-header">
                <div class="logo">
                    <i class="fas fa-cow" style="color: white;"></i>
                </div>
                <h2>Country Delight</h2>
            </div>
            
            <div class="nav-section">
                <div class="nav-title">Main Navigation</div>
                <div class="nav-item active">
                    <i class="fas fa-tachometer-alt"></i>
                    Dashboard
                </div>
                <div class="nav-item">
                    <i class="fas fa-users"></i>
                    Customers
                </div>
                <div class="nav-item">
                    <i class="fas fa-box"></i>
                    Subscriptions
                </div>
                <div class="nav-item">
                    <i class="fas fa-database"></i>
                    Customer Data
                </div>
            </div>
            
            <div class="nav-section">
                <div class="nav-title">Operations</div>
                <div class="nav-item">
                    <i class="fas fa-truck"></i>
                    Daily Deliveries
                </div>
                <div class="nav-item">
                    <i class="fas fa-calendar-alt"></i>
                    Delivery Schedule
                </div>
                <div class="nav-item">
                    <i class="fas fa-history"></i>
                    Delivery History
                </div>
            </div>
            
            <div class="nav-section">
                <div class="nav-title">Financial</div>
                <div class="nav-item">
                    <i class="fas fa-wallet"></i>
                    Prepaid Balance
                </div>
                <div class="nav-item">
                    <i class="fas fa-credit-card"></i>
                    Payments
                </div>
                <div class="nav-item">
                    <i class="fas fa-chart-bar"></i>
                    Reports
                </div>
            </div>
            
            <div class="nav-section">
                <div class="nav-title">System</div>
                <div class="nav-item">
                    <i class="fas fa-cog"></i>
                    Settings
                </div>
                <div class="nav-item">
                    <i class="fas fa-user-cog"></i>
                    User Management
                </div>
            </div>
        </div>
        
        <!-- Main Content -->
        <div class="main-content">
            <div class="header">
                <div class="header-title">
                    <i class="fas fa-tachometer-alt"></i>
                    Dashboard Overview
                </div>
                <div class="header-actions">
                    <input type="text" class="search-box" placeholder="Search customers, subscriptions...">
                    <button class="btn" id="refreshBtn">
                        <i class="fas fa-sync-alt"></i>
                        Refresh Data
                    </button>
                    <button class="btn btn-primary" id="addCustomerBtn">
                        <i class="fas fa-plus"></i>
                        Add New Customer
                    </button>
                </div>
            </div>
            
            <div class="content">
                <!-- Stats Grid -->
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-title">
                            <i class="fas fa-users"></i>
                            Active Subscriptions
                        </div>
                        <div class="stat-value">1,247</div>
                        <div class="stat-change positive">
                            <i class="fas fa-arrow-up"></i> 12% from last month
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-title">
                            <i class="fas fa-truck"></i>
                            Today's Deliveries
                        </div>
                        <div class="stat-value">892/1,247</div>
                        <div class="stat-change positive">
                            <i class="fas fa-check-circle"></i> 72% Completed
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-title">
                            <i class="fas fa-exclamation-triangle"></i>
                            Pending Payments
                        </div>
                        <div class="stat-value">₹84,520</div>
                        <div class="stat-change negative">
                            <i class="fas fa-arrow-up"></i> 8% from last week
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-title">
                            <i class="fas fa-wallet"></i>
                            Prepaid Balance
                        </div>
                        <div class="stat-value">₹2,45,780</div>
                        <div class="stat-change positive">
                            <i class="fas fa-arrow-up"></i> 15% from last month
                        </div>
                    </div>
                </div>
                
                <!-- Tabs -->
                <div class="tabs">
                    <div class="tab active">Active Subscriptions</div>
                    <div class="tab">Pending Deliveries</div>
                    <div class="tab">Low Balance</div>
                    <div class="tab">Suspended Accounts</div>
                </div>
                
                <!-- Subscription Table -->
                <div class="card">
                    <div class="card-header">
                        <div class="card-title">
                            <i class="fas fa-list"></i>
                            Active Subscriptions
                        </div>
                        <button class="btn" id="exportBtn">
                            <i class="fas fa-download"></i>
                            Export Data
                        </button>
                    </div>
                    <div class="card-body">
                        <table class="table">
                            <thead>
                                <tr>
                                    <th>Customer</th>
                                    <th>Subscription Type</th>
                                    <th>Start Date</th>
                                    <th>Next Delivery</th>
                                    <th>Balance</th>
                                    <th>Status</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>
                                        <div class="customer-info">
                                            <div class="customer-avatar">RS</div>
                                            <div class="customer-details">
                                                <div class="customer-name">Rahul Sharma</div>
                                                <div class="customer-id">CD-1001</div>
                                            </div>
                                        </div>
                                    </td>
                                    <td>Buffalo Milk - 2L Daily</td>
                                    <td>15 Jun 2023</td>
                                    <td>Tomorrow</td>
                                    <td>₹1,250</td>
                                    <td><span class="badge badge-success">Active</span></td>
                                    <td>
                                        <div class="action-btns">
                                            <button class="action-btn" title="Edit">
                                                <i class="fas fa-edit"></i>
                                            </button>
                                            <button class="action-btn" title="View Details">
                                                <i class="fas fa-eye"></i>
                                            </button>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <div class="customer-info">
                                            <div class="customer-avatar">PP</div>
                                            <div class="customer-details">
                                                <div class="customer-name">Priya Patel</div>
                                                <div class="customer-id">CD-1002</div>
                                            </div>
                                        </div>
                                    </td>
                                    <td>Cow Milk - 1L Daily</td>
                                    <td>22 May 2023</td>
                                    <td>Today</td>
                                    <td>₹680</td>
                                    <td><span class="badge badge-success">Active</span></td>
                                    <td>
                                        <div class="action-btns">
                                            <button class="action-btn" title="Edit">
                                                <i class="fas fa-edit"></i>
                                            </button>
                                            <button class="action-btn" title="View Details">
                                                <i class="fas fa-eye"></i>
                                            </button>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <div class="customer-info">
                                            <div class="customer-avatar">AK</div>
                                            <div class="customer-details">
                                                <div class="customer-name">Amit Kumar</div>
                                                <div class="customer-id">CD-1003</div>
                                            </div>
                                        </div>
                                    </td>
                                    <td>Buffalo Milk - 1L Daily</td>
                                    <td>10 Jul 2023</td>
                                    <td>Today</td>
                                    <td>₹320</td>
                                    <td><span class="badge badge-warning">Low Balance</span></td>
                                    <td>
                                        <div class="action-btns">
                                            <button class="action-btn" title="Edit">
                                                <i class="fas fa-edit"></i>
                                            </button>
                                            <button class="action-btn" title="View Details">
                                                <i class="fas fa-eye"></i>
                                            </button>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <div class="customer-info">
                                            <div class="customer-avatar">NG</div>
                                            <div class="customer-details">
                                                <div class="customer-name">Neha Gupta</div>
                                                <div class="customer-id">CD-1004</div>
                                            </div>
                                        </div>
                                    </td>
                                    <td>Cow Milk - 2L Daily</td>
                                    <td>05 Apr 2023</td>
                                    <td>Tomorrow</td>
                                    <td>₹0</td>
                                    <td><span class="badge badge-danger">Suspended</span></td>
                                    <td>
                                        <div class="action-btns">
                                            <button class="action-btn" title="Edit">
                                                <i class="fas fa-edit"></i>
                                            </button>
                                            <button class="action-btn" title="View Details">
                                                <i class="fas fa-eye"></i>
                                            </button>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        <div class="customer-info">
                                            <div class="customer-avatar">SS</div>
                                            <div class="customer-details">
                                                <div class="customer-name">Sanjay Singh</div>
                                                <div class="customer-id">CD-1005</div>
                                            </div>
                                        </div>
                                    </td>
                                    <td>Buffalo Milk - 1L Daily</td>
                                    <td>18 Aug 2023</td>
                                    <td>Today</td>
                                    <td>₹1,540</td>
                                    <td><span class="badge badge-success">Active</span></td>
                                    <td>
                                        <div class="action-btns">
                                            <button class="action-btn" title="Edit">
                                                <i class="fas fa-edit"></i>
                                            </button>
                                            <button class="action-btn" title="View Details">
                                                <i class="fas fa-eye"></i>
                                            </button>
                                        </div>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Add Customer Modal -->
    <div class="modal" id="addCustomerModal">
        <div class="modal-content">
            <div class="modal-header">
                <div class="modal-title">Add New Customer</div>
                <button class="modal-close" id="closeModal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label class="form-label">Full Name</label>
                    <input type="text" class="form-control" placeholder="Enter customer full name">
                </div>
                <div class="form-group">
                    <label class="form-label">Phone Number</label>
                    <input type="tel" class="form-control" placeholder="Enter phone number">
                </div>
                <div class="form-group">
                    <label class="form-label">Email Address</label>
                    <input type="email" class="form-control" placeholder="Enter email address">
                </div>
                <div class="form-group">
                    <label class="form-label">Delivery Address</label>
                    <textarea class="form-control" rows="3" placeholder="Enter complete delivery address"></textarea>
                </div>
                <div class="form-group">
                    <label class="form-label">Subscription Type</label>
                    <select class="form-control">
                        <option value="">Select subscription plan</option>
                        <option value="cow-1l">Cow Milk - 1L Daily</option>
                        <option value="cow-2l">Cow Milk - 2L Daily</option>
                        <option value="buffalo-1l">Buffalo Milk - 1L Daily</option>
                        <option value="buffalo-2l">Buffalo Milk - 2L Daily</option>
                    </select>
                </div>
                <div class="form-group">
                    <label class="form-label">Initial Payment Amount</label>
                    <input type="number" class="form-control" placeholder="Enter initial payment amount">
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn" id="cancelBtn">Cancel</button>
                <button class="btn btn-primary">Add Customer</button>
            </div>
        </div>
    </div>

    <script>
        // JavaScript for interactive functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Modal functionality
            const addCustomerBtn = document.getElementById('addCustomerBtn');
            const addCustomerModal = document.getElementById('addCustomerModal');
            const closeModal = document.getElementById('closeModal');
            const cancelBtn = document.getElementById('cancelBtn');
            
            addCustomerBtn.addEventListener('click', () => {
                addCustomerModal.style.display = 'flex';
            });
            
            closeModal.addEventListener('click', () => {
                addCustomerModal.style.display = 'none';
            });
            
            cancelBtn.addEventListener('click', () => {
                addCustomerModal.style.display = 'none';
            });
            
            // Close modal when clicking outside
            window.addEventListener('click', (event) => {
                if (event.target === addCustomerModal) {
                    addCustomerModal.style.display = 'none';
                }
            });
            
            // Tab functionality
            const tabs = document.querySelectorAll('.tab');
            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    tabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');
                });
            });
            
            // Navigation functionality
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => {
                item.addEventListener('click', () => {
                    navItems.forEach(i => i.classList.remove('active'));
                    item.classList.add('active');
                });
            });
            
            // Refresh button functionality
            const refreshBtn = document.getElementById('refreshBtn');
            refreshBtn.addEventListener('click', function() {
                const icon = this.querySelector('i');
                icon.className = 'fas fa-spinner loading';
                
                setTimeout(() => {
                    icon.className = 'fas fa-sync-alt';
                    alert('Data refreshed successfully!');
                }, 1500);
            });
            
            // Export button functionality
            const exportBtn = document.getElementById('exportBtn');
            exportBtn.addEventListener('click', function() {
                alert('Exporting data to CSV...');
            });
            
            // Search functionality
            const searchBox = document.querySelector('.search-box');
            searchBox.addEventListener('input', function(e) {
                const searchTerm = e.target.value.toLowerCase();
                console.log('Searching for:', searchTerm);
            });
            
            // Auto-update simulation
            setInterval(() => {
                console.log('Auto-update check...');
            }, 30000);
        });
    </script>
</body>
</html>
