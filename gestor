<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Minhas Finanças Pessoais</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2ecc71;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --paid-color: #2ecc71;
            --pending-color: #e74c3c;
            --overdue-color: #34495e;
            --sidebar-width: 250px;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f7fa;
            margin: 0;
            padding: 0;
            color: var(--dark-color);
            -webkit-text-size-adjust: 100%;
        }
        
        .login-container {
            width: 90%;
            max-width: 400px;
            margin: 50px auto;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .login-logo {
            margin-bottom: 20px;
        }
        
        .login-logo i {
            font-size: 3rem;
            color: var(--primary-color);
        }
        
        .login-container h1 {
            color: var(--primary-color);
            margin-bottom: 20px;
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
            font-size: 1.5rem;
        }
        
        .login-form input {
            width: 100%;
            padding: 12px 15px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            box-sizing: border-box;
        }
        
        .login-form button {
            width: 100%;
            padding: 12px;
            background-color: var(--secondary-color);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .login-form button:hover {
            background-color: #27ad60;
        }
        
        .error-message {
            color: var(--accent-color);
            margin-bottom: 15px;
            display: none;
        }
        
        /* Layout principal */
        .app-wrapper {
            display: flex;
            min-height: 100vh;
        }
        
        /* Sidebar */
        .sidebar {
            width: var(--sidebar-width);
            background-color: var(--dark-color);
            color: white;
            padding: 20px 0;
            transition: all 0.3s;
            position: fixed;
            height: 100vh;
            overflow-y: auto;
        }
        
        .sidebar-header {
            text-align: center;
            padding: 0 20px 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .app-logo {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            color: white;
            text-decoration: none;
        }
        
        .app-logo i {
            font-size: 2rem;
            margin-right: 10px;
            color: var(--secondary-color);
        }
        
        .app-logo span {
            font-size: 1.2rem;
            font-weight: bold;
        }
        
        .sidebar-menu {
            padding: 20px 0;
        }
        
        .menu-item {
            padding: 12px 20px;
            display: flex;
            align-items: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .menu-item:hover, .menu-item.active {
            background-color: rgba(255, 255, 255, 0.1);
            border-left: 3px solid var(--secondary-color);
        }
        
        .menu-item i {
            margin-right: 10px;
            width: 20px;
            text-align: center;
        }
        
        /* Main content */
        .main-content {
            flex: 1;
            margin-left: var(--sidebar-width);
            padding: 20px;
        }
        
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .page-title {
            color: var(--primary-color);
            margin: 0;
        }
        
        .user-profile {
            display: flex;
            align-items: center;
        }
        
        .profile-pic {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--primary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 10px;
            cursor: pointer;
        }
        
        .profile-dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            z-index: 1;
            border-radius: 5px;
            padding: 10px 0;
        }
        
        .profile-dropdown:hover .dropdown-content {
            display: block;
        }
        
        .dropdown-item {
            padding: 10px 15px;
            display: block;
            color: var(--dark-color);
            text-decoration: none;
        }
        
        .dropdown-item:hover {
            background-color: #f5f5f5;
        }
        
        .dropdown-divider {
            height: 1px;
            background-color: #eee;
            margin: 5px 0;
        }
        
        /* Container principal */
        .container {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin-bottom: 20px;
        }
        
        /* Dashboard cards */
        .dashboard {
            display: flex;
            flex-direction: column;
            margin-bottom: 20px;
        }
        
        .card {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            padding: 15px;
            margin-bottom: 10px;
            border-top: 4px solid var(--secondary-color);
            position: relative;
        }
        
        .card h2 {
            color: var(--primary-color);
            font-size: 1.1rem;
            margin-top: 0;
            display: flex;
            align-items: center;
        }
        
        .card h2 i {
            margin-right: 8px;
        }
        
        /* Tabelas */
        table {
            border-collapse: collapse;
            width: 100%;
            margin: 15px 0;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            font-size: 0.9rem;
        }
        
        th, td {
            border: 1px solid #ddd;
            padding: 8px 10px;
            text-align: left;
        }
        
        th {
            background-color: var(--primary-color);
            color: white;
            font-weight: 600;
            font-size: 0.9rem;
        }
        
        tr:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        tr:hover {
            background-color: #f1f1f1;
        }
        
        .total {
            font-weight: bold;
            color: var(--success-color);
        }
        
        .status-paid {
            background-color: rgba(46, 204, 113, 0.1);
        }
        
        .status-pending {
            background-color: rgba(231, 76, 60, 0.1);
        }
        
        .status-overdue {
            background-color: rgba(52, 73, 94, 0.1);
        }
        
        .status-indicator {
            display: inline-block;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 6px;
        }
        
        .paid {
            background-color: var(--paid-color);
        }
        
        .pending {
            background-color: var(--pending-color);
        }
        
        .overdue {
            background-color: var(--overdue-color);
        }
        
        /* Formulários */
        .add-expense-form {
            margin: 20px 0;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }
        
        .form-row {
            margin-bottom: 15px;
        }
        
        .form-row label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
            color: var(--primary-color);
        }
        
        .form-row input, .form-row select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            box-sizing: border-box;
        }
        
        .add-btn {
            background-color: var(--success-color);
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            width: 100%;
            transition: background-color 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .add-btn i {
            margin-right: 8px;
        }
        
        .add-btn:hover {
            background-color: #219955;
        }
        
        /* Orçamento */
        .remaining-budget {
            background-color: #e8f4fd;
            border-left: 4px solid var(--secondary-color);
            padding: 15px;
            margin: 15px 0;
            border-radius: 0 5px 5px 0;
        }
        
        .remaining-budget h3 {
            margin-top: 0;
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }
        
        .remaining-budget h3 i {
            margin-right: 8px;
        }
        
        .budget-input {
            display: flex;
            gap: 10px;
            margin-bottom: 10px;
        }
        
        .budget-input input {
            flex: 1;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        .budget-input button {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            border-radius: 4px;
            padding: 0 15px;
            cursor: pointer;
            display: flex;
            align-items: center;
        }
        
        .budget-summary {
            margin-top: 10px;
        }
        
        .budget-summary p {
            margin: 5px 0;
            display: flex;
            justify-content: space-between;
        }
        
        .budget-summary span {
            font-weight: 600;
        }
        
        .positive {
            color: var(--success-color);
        }
        
        .negative {
            color: var(--accent-color);
        }
        
        /* Legendas */
        .status-legend {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 15px 0;
            flex-wrap: wrap;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.8rem;
        }
        
        /* Botões */
        .delete-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            border-radius: 3px;
            padding: 3px 6px;
            cursor: pointer;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
        }
        
        .delete-btn i {
            margin-right: 4px;
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4);
            overflow: auto;
        }
        
        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 20px;
            border-radius: 8px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .modal-header h2 {
            margin: 0;
            color: var(--primary-color);
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #999;
        }
        
        .modal-body {
            margin-bottom: 20px;
        }
        
        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 10px;
        }
        
        .modal-btn {
            padding: 8px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9rem;
        }
        
        .modal-btn-primary {
            background-color: var(--primary-color);
            color: white;
        }
        
        .modal-btn-secondary {
            background-color: #ddd;
            color: #333;
        }
        
        /* Página de perfil */
        .profile-container {
            display: flex;
            flex-direction: column;
        }
        
        .profile-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eee;
        }
        
        .profile-avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: var(--primary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-right: 20px;
        }
        
        .profile-info {
            flex: 1;
        }
        
        .profile-info h2 {
            margin: 0 0 5px;
            color: var(--dark-color);
        }
        
        .profile-info p {
            margin: 0;
            color: #777;
        }
        
        .profile-section {
            margin-bottom: 30px;
        }
        
        .profile-section h3 {
            color: var(--primary-color);
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
            margin-bottom: 15px;
        }
        
        .form-group {
            margin-bottom: 15px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
            color: var(--dark-color);
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .save-btn {
            background-color: var(--success-color);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }
        
        /* Gráficos */
        .chart-container {
            height: 300px;
            margin: 20px 0;
            position: relative;
        }
        
        .chart-placeholder {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            color: #777;
        }
        
        /* Responsividade */
        @media (min-width: 768px) {
            .login-container {
                margin: 100px auto;
                padding: 30px;
            }
            
            .dashboard {
                flex-direction: row;
                justify-content: space-between;
            }
            
            .card {
                min-width: 30%;
                margin: 0 5px;
            }
            
            .form-row {
                display: flex;
                align-items: center;
            }
            
            .form-row label {
                width: 120px;
                margin-bottom: 0;
                margin-right: 10px;
            }
            
            .form-row input, .form-row select {
                flex: 1;
            }
            
            .add-btn {
                width: auto;
            }
            
            .profile-container {
                flex-direction: row;
                flex-wrap: wrap;
            }
            
            .profile-main {
                flex: 2;
                margin-right: 20px;
            }
            
            .profile-sidebar {
                flex: 1;
            }
        }
        
        @media (max-width: 768px) {
            .sidebar {
                width: 0;
                overflow: hidden;
                position: fixed;
                z-index: 1000;
            }
            
            .sidebar.active {
                width: var(--sidebar-width);
            }
            
            .main-content {
                margin-left: 0;
            }
            
            .menu-toggle {
                display: block;
                font-size: 1.5rem;
                cursor: pointer;
                margin-right: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Tela de Login -->
    <div class="login-container" id="loginContainer">
        <div class="login-logo">
            <i class="fas fa-wallet"></i>
        </div>
        <h1>Acesso ao Sistema</h1>
        <p class="error-message" id="errorMessage">E-mail ou senha incorretos</p>
        <form class="login-form" id="loginForm">
            <input type="email" id="email" placeholder="E-mail" required>
            <input type="password" id="password" placeholder="Senha" required>
            <button type="submit">Entrar</button>
        </form>
        <p style="margin-top: 20px;">Não tem uma conta? <a href="#" onclick="showRegisterModal()">Cadastre-se</a></p>
    </div>
    
    <!-- Aplicação Principal -->
    <div class="app-wrapper" id="appWrapper" style="display: none;">
        <!-- Sidebar -->
        <div class="sidebar" id="sidebar">
            <div class="sidebar-header">
                <a href="#" class="app-logo">
                    <i class="fas fa-wallet"></i>
                    <span>Minhas Finanças</span>
                </a>
            </div>
            
            <div class="sidebar-menu">
                <a href="#" class="menu-item active" onclick="showSection('dashboard')">
                    <i class="fas fa-home"></i>
                    <span>Dashboard</span>
                </a>
                <a href="#" class="menu-item" onclick="showSection('expenses')">
                    <i class="fas fa-list"></i>
                    <span>Despesas</span>
                </a>
                <a href="#" class="menu-item" onclick="showSection('budget')">
                    <i class="fas fa-chart-pie"></i>
                    <span>Orçamento</span>
                </a>
                <a href="#" class="menu-item" onclick="showSection('reports')">
                    <i class="fas fa-chart-bar"></i>
                    <span>Relatórios</span>
                </a>
                <a href="#" class="menu-item" onclick="showSection('profile')">
                    <i class="fas fa-user"></i>
                    <span>Meu Perfil</span>
                </a>
            </div>
        </div>
        
        <!-- Conteúdo Principal -->
        <div class="main-content">
            <!-- Header -->
            <div class="header">
                <div class="menu-toggle" onclick="toggleSidebar()">
                    <i class="fas fa-bars"></i>
                </div>
                <h1 class="page-title" id="pageTitle">Dashboard</h1>
                <div class="user-profile">
                    <div class="profile-dropdown">
                        <div class="profile-pic" id="profilePic">
                            <i class="fas fa-user"></i>
                        </div>
                        <div class="dropdown-content">
                            <div class="dropdown-item" onclick="showSection('profile')">
                                <i class="fas fa-user-circle"></i> Meu Perfil
                            </div>
                            <div class="dropdown-item" onclick="openChangePasswordModal()">
                                <i class="fas fa-key"></i> Alterar Senha
                            </div>
                            <div class="dropdown-divider"></div>
                            <div class="dropdown-item" onclick="logout()">
                                <i class="fas fa-sign-out-alt"></i> Sair
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Seções da aplicação -->
            <div id="sections">
                <!-- Dashboard -->
                <div class="section" id="dashboardSection">
                    <div class="status-legend">
                        <div class="legend-item">
                            <div class="status-indicator paid"></div>
                            <span>Pago</span>
                        </div>
                        <div class="legend-item">
                            <div class="status-indicator pending"></div>
                            <span>Pendente</span>
                        </div>
                        <div class="legend-item">
                            <div class="status-indicator overdue"></div>
                            <span>Atrasado</span>
                        </div>
                    </div>
                    
                    <div class="dashboard">
                        <div class="card">
                            <h2><i class="fas fa-home"></i> Despesas Fixas</h2>
                            <p id="fixedExpenses">R$ 0,00</p>
                        </div>
                        <div class="card">
                            <h2><i class="fas fa-shopping-cart"></i> Despesas Variáveis</h2>
                            <p id="variableExpenses">R$ 0,00</p>
                        </div>
                        <div class="card">
                            <h2><i class="fas fa-coins"></i> Total Mensal</h2>
                            <p class="total" id="totalExpenses">R$ 0,00</p>
                        </div>
                    </div>
                    
                    <div class="container">
                        <h2><i class="fas fa-chart-line"></i> Resumo Mensal</h2>
                        <div class="chart-container" id="monthlyChart">
                            <div class="chart-placeholder">
                                <i class="fas fa-chart-pie" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                                <p>Gráfico de resumo mensal</p>
                                <p style="font-size: 0.8rem;">(Dados serão exibidos conforme as despesas são cadastradas)</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="remaining-budget">
                        <h3><i class="fas fa-wallet"></i> Valores a Gastar</h3>
                        <div class="budget-input">
                            <input type="number" id="monthlyBudget" placeholder="Orçamento mensal" step="0.01" min="0">
                            <button onclick="setBudget()"><i class="fas fa-check"></i></button>
                        </div>
                        <div class="budget-summary">
                            <p>Orçamento: <span id="budgetAmount">R$ 0,00</span></p>
                            <p>Gasto total: <span id="spentAmount">R$ 0,00</span></p>
                            <p>Restante: <span id="remainingAmount" class="positive">R$ 0,00</span></p>
                        </div>
                    </div>
                </div>
                
                <!-- Despesas -->
                <div class="section" id="expensesSection" style="display: none;">
                    <div class="container">
                        <h2><i class="fas fa-list"></i> Todas as Despesas</h2>
                        
                        <div style="margin-bottom: 20px; display: flex; gap: 10px;">
                            <select id="filterCategory" class="form-control" style="flex: 1;">
                                <option value="">Todas categorias</option>
                                <option value="Despesas fixas">Despesas fixas</option>
                                <option value="Despesas variáveis">Despesas variáveis</option>
                                <option value="Moradia">Moradia</option>
                                <option value="Alimentação">Alimentação</option>
                                <option value="Transporte">Transporte</option>
                                <option value="Saúde">Saúde</option>
                                <option value="Educação">Educação</option>
                                <option value="Lazer">Lazer</option>
                                <option value="Outros">Outros</option>
                            </select>
                            
                            <select id="filterStatus" class="form-control" style="flex: 1;">
                                <option value="">Todos status</option>
                                <option value="paid">Pago</option>
                                <option value="pending">Pendente</option>
                                <option value="overdue">Atrasado</option>
                            </select>
                            
                            <button onclick="filterExpenses()" style="padding: 0 15px;">
                                <i class="fas fa-filter"></i> Filtrar
                            </button>
                            
                            <button onclick="resetFilters()" style="padding: 0 15px;">
                                <i class="fas fa-times"></i> Limpar
                            </button>
                        </div>
                        
                        <table>
                            <thead>
                                <tr>
                                    <th>Data</th>
                                    <th>Status</th>
                                    <th>Descrição</th>
                                    <th>Valor</th>
                                    <th>Categoria</th>
                                    <th>Ações</th>
                                </tr>
                            </thead>
                            <tbody id="expensesTableBody">
                                <!-- Dados serão carregados dinamicamente -->
                            </tbody>
                        </table>
                    </div>
                    
                    <div class="container">
                        <h2><i class="fas fa-plus-circle"></i> Adicionar Nova Despesa</h2>
                        <div class="add-expense-form">
                            <div class="form-row">
                                <label for="expenseDate">Data:</label>
                                <input type="date" id="expenseDate" required>
                            </div>
                            <div class="form-row">
                                <label for="expenseDescription">Descrição:</label>
                                <input type="text" id="expenseDescription" placeholder="Descrição da despesa" required>
                            </div>
                            <div class="form-row">
                                <label for="expenseValue">Valor:</label>
                                <input type="number" id="expenseValue" placeholder="0,00" step="0.01" min="0" required>
                            </div>
                            <div class="form-row">
                                <label for="expenseCategory">Categoria:</label>
                                <select id="expenseCategory" required>
                                    <option value="Despesas fixas">Despesas fixas</option>
                                    <option value="Despesas variáveis">Despesas variáveis</option>
                                    <option value="Moradia">Moradia</option>
                                    <option value="Alimentação">Alimentação</option>
                                    <option value="Transporte">Transporte</option>
                                    <option value="Saúde">Saúde</option>
                                    <option value="Educação">Educação</option>
                                    <option value="Lazer">Lazer</option>
                                    <option value="Outros">Outros</option>
                                </select>
                            </div>
                            <div class="form-row">
                                <label for="expenseStatus">Status:</label>
                                <select id="expenseStatus" required>
                                    <option value="paid">Pago</option>
                                    <option value="pending">Pendente</option>
                                    <option value="overdue">Atrasado</option>
                                </select>
                            </div>
                            <button class="add-btn" onclick="addExpense()">
                                <i class="fas fa-plus"></i> Adicionar Despesa
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Orçamento -->
                <div class="section" id="budgetSection" style="display: none;">
                    <div class="container">
                        <h2><i class="fas fa-chart-pie"></i> Meu Orçamento</h2>
                        
                        <div class="chart-container" id="budgetChart">
                            <div class="chart-placeholder">
                                <i class="fas fa-chart-pie" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                                <p>Gráfico de distribuição do orçamento</p>
                                <p style="font-size: 0.8rem;">(Dados serão exibidos conforme o orçamento é definido)</p>
                            </div>
                        </div>
                        
                        <div class="remaining-budget">
                            <h3><i class="fas fa-wallet"></i> Controle de Orçamento</h3>
                            <div class="budget-input">
                                <input type="number" id="monthlyBudget2" placeholder="Orçamento mensal" step="0.01" min="0">
                                <button onclick="setBudget()"><i class="fas fa-check"></i></button>
                            </div>
                            <div class="budget-summary">
                                <p>Orçamento: <span id="budgetAmount2">R$ 0,00</span></p>
                                <p>Gasto total: <span id="spentAmount2">R$ 0,00</span></p>
                                <p>Restante: <span id="remainingAmount2" class="positive">R$ 0,00</span></p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Relatórios -->
                <div class="section" id="reportsSection" style="display: none;">
                    <div class="container">
                        <h2><i class="fas fa-chart-bar"></i> Relatórios</h2>
                        
                        <div style="margin-bottom: 20px; display: flex; gap: 10px; flex-wrap: wrap;">
                            <select id="reportType" class="form-control" style="flex: 1; min-width: 200px;">
                                <option value="monthly">Relatório Mensal</option>
                                <option value="category">Por Categoria</option>
                                <option value="status">Por Status</option>
                            </select>
                            
                            <select id="reportMonth" class="form-control" style="flex: 1; min-width: 150px;">
                                <option value="1">Janeiro</option>
                                <option value="2">Fevereiro</option>
                                <option value="3">Março</option>
                                <option value="4">Abril</option>
                                <option value="5">Maio</option>
                                <option value="6">Junho</option>
                                <option value="7">Julho</option>
                                <option value="8">Agosto</option>
                                <option value="9">Setembro</option>
                                <option value="10">Outubro</option>
                                <option value="11">Novembro</option>
                                <option value="12">Dezembro</option>
                            </select>
                            
                            <select id="reportYear" class="form-control" style="flex: 1; min-width: 120px;">
                                <option value="2023">2023</option>
                                <option value="2024">2024</option>
                                <option value="2025">2025</option>
                            </select>
                            
                            <button onclick="generateReport()" style="padding: 0 15px; min-width: 100px;">
                                <i class="fas fa-chart-bar"></i> Gerar
                            </button>
                            
                            <button onclick="exportReport()" style="padding: 0 15px; min-width: 100px;">
                                <i class="fas fa-file-export"></i> Exportar
                            </button>
                        </div>
                        
                        <div class="chart-container" id="reportChart">
                            <div class="chart-placeholder">
                                <i class="fas fa-chart-bar" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                                <p>Selecione as opções e gere o relatório</p>
                            </div>
                        </div>
                        
                        <div id="reportTableContainer" style="display: none; margin-top: 20px;">
                            <h3>Dados do Relatório</h3>
                            <table id="reportTable">
                                <thead>
                                    <tr>
                                        <th>Descrição</th>
                                        <th>Valor</th>
                                        <th>Categoria</th>
                                        <th>Status</th>
                                    </tr>
                                </thead>
                                <tbody id="reportTableBody">
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
                
                <!-- Perfil do Usuário -->
                <div class="section" id="profileSection" style="display: none;">
                    <div class="container">
                        <div class="profile-header">
                            <div class="profile-avatar" id="profileAvatar">
                                <i class="fas fa-user"></i>
                            </div>
                            <div class="profile-info">
                                <h2 id="profileName">Usuário</h2>
                                <p id="profileEmail">email@exemplo.com</p>
                                <p id="profileSince" style="font-size: 0.8rem; color: #999;">Membro desde: <span id="memberSince"></span></p>
                            </div>
                        </div>
                        
                        <div class="profile-container">
                            <div class="profile-main">
                                <div class="profile-section">
                                    <h3><i class="fas fa-user-edit"></i> Informações Pessoais</h3>
                                    
                                    <div class="form-group">
                                        <label for="userName">Nome:</label>
                                        <input type="text" id="userName" placeholder="Seu nome completo">
                                    </div>
                                    
                                    <div class="form-group">
                                        <label for="userPhone">Telefone:</label>
                                        <input type="tel" id="userPhone" placeholder="(00) 00000-0000">
                                    </div>
                                    
                                    <div class="form-group">
                                        <label for="userBirthday">Data de Nascimento:</label>
                                        <input type="date" id="userBirthday">
                                    </div>
                                    
                                    <button class="save-btn" onclick="saveProfile()">
                                        <i class="fas fa-save"></i> Salvar Alterações
                                    </button>
                                </div>
                                
                                <div class="profile-section">
                                    <h3><i class="fas fa-bell"></i> Notificações</h3>
                                    
                                    <div class="form-group" style="display: flex; align-items: center;">
                                        <input type="checkbox" id="notifyExpenses" style="width: auto; margin-right: 10px;">
                                        <label for="notifyExpenses" style="margin-bottom: 0;">Receber alertas de despesas próximas do vencimento</label>
                                    </div>
                                    
                                    <div class="form-group" style="display: flex; align-items: center;">
                                        <input type="checkbox" id="notifyReports" style="width: auto; margin-right: 10px;">
                                        <label for="notifyReports" style="margin-bottom: 0;">Receber relatório mensal por e-mail</label>
                                    </div>
                                    
                                    <div class="form-group" style="display: flex; align-items: center;">
                                        <input type="checkbox" id="notifyBudget" style="width: auto; margin-right: 10px;">
                                        <label for="notifyBudget" style="margin-bottom: 0;">Receber alertas quando o orçamento estiver próximo do limite</label>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="profile-sidebar">
                                <div class="profile-section">
                                    <h3><i class="fas fa-cog"></i> Configurações</h3>
                                    
                                    <div class="form-group">
                                        <label for="userCurrency">Moeda:</label>
                                        <select id="userCurrency">
                                            <option value="BRL">Real Brasileiro (R$)</option>
                                            <option value="USD">Dólar Americano ($)</option>
                                            <option value="EUR">Euro (€)</option>
                                        </select>
                                    </div>
                                    
                                    <div class="form-group">
                                        <label for="userLanguage">Idioma:</label>
                                        <select id="userLanguage">
                                            <option value="pt-BR">Português (Brasil)</option>
                                            <option value="en-US">Inglês (EUA)</option>
                                            <option value="es-ES">Espanhol</option>
                                        </select>
                                    </div>
                                    
                                    <div class="form-group">
                                        <label for="userTheme">Tema:</label>
                                        <select id="userTheme">
                                            <option value="light">Claro</option>
                                            <option value="dark">Escuro</option>
                                            <option value="system">Sistema</option>
                                        </select>
                                    </div>
                                </div>
                                
                                <div class="profile-section">
                                    <h3><i class="fas fa-shield-alt"></i> Segurança</h3>
                                    
                                    <button class="save-btn" onclick="openChangePasswordModal()" style="width: 100%;">
                                        <i class="fas fa-key"></i> Alterar Senha
                                    </button>
                                    
                                    <button class="save-btn" onclick="exportUserData()" style="width: 100%; margin-top: 10px; background-color: var(--primary-color);">
                                        <i class="fas fa-file-export"></i> Exportar Meus Dados
                                    </button>
                                    
                                    <button class="save-btn" onclick="confirmAccountDeletion()" style="width: 100%; margin-top: 10px; background-color: var(--accent-color);">
                                        <i class="fas fa-trash-alt"></i> Excluir Minha Conta
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Modal para alteração de senha -->
    <div id="passwordModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2><i class="fas fa-key"></i> Alterar Senha</h2>
                <button class="close-modal" onclick="closeModal()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="currentPassword">Senha Atual:</label>
                    <input type="password" id="currentPassword" placeholder="Digite sua senha atual" required>
                </div>
                <div class="form-group">
                    <label for="newPassword">Nova Senha:</label>
                    <input type="password" id="newPassword" placeholder="Digite a nova senha" required>
                </div>
                <div class="form-group">
                    <label for="confirmPassword">Confirmar Nova Senha:</label>
                    <input type="password" id="confirmPassword" placeholder="Confirme a nova senha" required>
                </div>
            </div>
            <div class="modal-footer">
                <button class="modal-btn modal-btn-secondary" onclick="closeModal()">Cancelar</button>
                <button class="modal-btn modal-btn-primary" onclick="changePassword()">Salvar Alterações</button>
            </div>
        </div>
    </div>
    
    <!-- Modal para cadastro de novo usuário -->
    <div id="registerModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2><i class="fas fa-user-plus"></i> Cadastro de Novo Usuário</h2>
                <button class="close-modal" onclick="closeModal()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="registerName">Nome Completo:</label>
                    <input type="text" id="registerName" placeholder="Digite seu nome completo" required>
                </div>
                <div class="form-group">
                    <label for="registerEmail">E-mail:</label>
                    <input type="email" id="registerEmail" placeholder="Digite seu e-mail" required>
                </div>
                <div class="form-group">
                    <label for="registerPassword">Senha:</label>
                    <input type="password" id="registerPassword" placeholder="Digite uma senha" required>
                </div>
                <div class="form-group">
                    <label for="registerConfirmPassword">Confirmar Senha:</label>
                    <input type="password" id="registerConfirmPassword" placeholder="Confirme a senha" required>
                </div>
            </div>
            <div class="modal-footer">
                <button class="modal-btn modal-btn-secondary" onclick="closeModal()">Cancelar</button>
                <button class="modal-btn modal-btn-primary" onclick="registerUser()">Cadastrar</button>
            </div>
        </div>
    </div>
    
    <!-- Modal para confirmação de exclusão de conta -->
    <div id="deleteAccountModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2><i class="fas fa-exclamation-triangle"></i> Confirmar Exclusão</h2>
                <button class="close-modal" onclick="closeModal()">&times;</button>
            </div>
            <div class="modal-body">
                <p>Tem certeza que deseja excluir sua conta? Todos os seus dados serão permanentemente removidos e essa ação não pode ser desfeita.</p>
                <div class="form-group">
                    <label for="deletePassword">Digite sua senha para confirmar:</label>
                    <input type="password" id="deletePassword" placeholder="Sua senha" required>
                </div>
            </div>
            <div class="modal-footer">
                <button class="modal-btn modal-btn-secondary" onclick="closeModal()">Cancelar</button>
                <button class="modal-btn" onclick="deleteAccount()" style="background-color: var(--accent-color); color: white;">Excluir Conta</button>
            </div>
        </div>
    </div>

    <script>
        // Elementos do DOM
        const loginContainer = document.getElementById('loginContainer');
        const appWrapper = document.getElementById('appWrapper');
        const loginForm = document.getElementById('loginForm');
        const errorMessage = document.getElementById('errorMessage');
        const profilePic = document.getElementById('profilePic');
        const passwordModal = document.getElementById('passwordModal');
        const registerModal = document.getElementById('registerModal');
        const deleteAccountModal = document.getElementById('deleteAccountModal');
        const expensesTableBody = document.getElementById('expensesTableBody');
        const monthlyBudgetInput = document.getElementById('monthlyBudget');
        const monthlyBudgetInput2 = document.getElementById('monthlyBudget2');
        const sidebar = document.getElementById('sidebar');
        
        // Dados iniciais de usuários
        const initialUsers = {
            'jmpaivateles@gmail.com': {
                password: 'joselia23',
                name: 'José Maria Paiva Teles',
                phone: '',
                birthday: '',
                registrationDate: new Date().toISOString(),
                expenses: [],
                budget: 0,
                currency: 'BRL',
                language: 'pt-BR',
                theme: 'light',
                notifications: {
                    expenses: true,
                    reports: true,
                    budget: true
                }
            },
            'carlosalexandredepaivacaldeira@gmail.com': {
                password: 'carlos18',
                name: 'Carlos Alexandre de Paiva Caldeira',
                phone: '',
                birthday: '',
                registrationDate: new Date().toISOString(),
                expenses: [],
                budget: 0,
                currency: 'BRL',
                language: 'pt-BR',
                theme: 'light',
                notifications: {
                    expenses: true,
                    reports: true,
                    budget: true
                }
            }
        };
        
        // Carregar ou inicializar dados dos usuários
        function loadUsersData() {
            const savedUsers = localStorage.getItem('financeAppUsers');
            if (savedUsers) {
                return JSON.parse(savedUsers);
            } else {
                localStorage.setItem('financeAppUsers', JSON.stringify(initialUsers));
                return initialUsers;
            }
        }
        
        // Salvar dados dos usuários
        function saveUsersData(users) {
            localStorage.setItem('financeAppUsers', JSON.stringify(users));
        }
        
        // Obter dados atuais dos usuários
        let usersData = loadUsersData();
        
        // Verificar se há usuário logado ao carregar a página
        document.addEventListener('DOMContentLoaded', function() {
            const loggedInUser = localStorage.getItem('loggedInUser');
            
            if (loggedInUser) {
                loginContainer.style.display = 'none';
                appWrapper.style.display = 'flex';
                
                // Carregar dados do usuário
                loadUserData();
                updateProfileDisplay();
                
                // Aplicar tema salvo
                applyTheme();
            } else {
                loginContainer.style.display = 'block';
                appWrapper.style.display = 'none';
            }
            
            // Configurar data padrão para hoje
            document.getElementById('expenseDate').valueAsDate = new Date();
            
            // Configurar ano atual como padrão no relatório
            const currentYear = new Date().getFullYear();
            const reportYearSelect = document.getElementById('reportYear');
            const currentMonth = new Date().getMonth() + 1;
            document.getElementById('reportMonth').value = currentMonth;
            
            // Verificar se o ano atual está nas opções
            let yearExists = false;
            for (let i = 0; i < reportYearSelect.options.length; i++) {
                if (parseInt(reportYearSelect.options[i].value) === currentYear) {
                    yearExists = true;
                    break;
                }
            }
            
            if (!yearExists) {
                const newOption = document.createElement('option');
                newOption.value = currentYear;
                newOption.textContent = currentYear;
                reportYearSelect.appendChild(newOption);
            }
            
            reportYearSelect.value = currentYear;
        });
        
        // Processar formulário de login
        loginForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const email = document.getElementById('email').value.trim().toLowerCase();
            const password = document.getElementById('password').value;
            
            if (usersData[email] && usersData[email].password === password) {
                // Login bem-sucedido
                localStorage.setItem('loggedInUser', email);
                loginContainer.style.display = 'none';
                appWrapper.style.display = 'flex';
                errorMessage.style.display = 'none';
                
                // Carregar dados do usuário
                loadUserData();
                updateProfileDisplay();
                applyTheme();
            } else {
                // Login falhou
                errorMessage.style.display = 'block';
            }
        });
        
        // Função para carregar dados do usuário
        function loadUserData() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const user = usersData[userEmail];
            const expenses = user.expenses;
            
            // Limpar tabela
            expensesTableBody.innerHTML = '';
            
            let fixedTotal = 0;
            let variableTotal = 0;
            let totalSpent = 0;
            
            // Ordenar despesas por data (mais recente primeiro)
            expenses.sort((a, b) => new Date(b.date) - new Date(a.date));
            
            // Preencher tabela com despesas
            expenses.forEach((expense, index) => {
                const row = document.createElement('tr');
                row.classList.add(`status-${expense.status}`);
                
                // Formatar data para exibição (dd/mm/aaaa)
                const dateObj = new Date(expense.date);
                const formattedDate = dateObj.toLocaleDateString('pt-BR');
                
                // Atualizar totais
                const value = parseFloat(expense.value);
                totalSpent += value;
                
                if (expense.category === 'Despesas fixas') {
                    fixedTotal += value;
                } else {
                    variableTotal += value;
                }
                
                row.innerHTML = `
                    <td>${formattedDate}</td>
                    <td>
                        <select class="status-select" onchange="updateStatus(this, ${index})">
                            <option value="paid" ${expense.status === 'paid' ? 'selected' : ''}>Pago</option>
                            <option value="pending" ${expense.status === 'pending' ? 'selected' : ''}>Pendente</option>
                            <option value="overdue" ${expense.status === 'overdue' ? 'selected' : ''}>Atrasado</option>
                        </select>
                    </td>
                    <td>${expense.description}</td>
                    <td>R$ ${value.toFixed(2).replace('.', ',')}</td>
                    <td>${expense.category}</td>
                    <td><button class="delete-btn" onclick="deleteExpense(${index})"><i class="fas fa-trash"></i> Excluir</button></td>
                `;
                
                expensesTableBody.appendChild(row);
            });
            
            // Atualizar totais no dashboard
            updateTotals(fixedTotal, variableTotal);
            
            // Atualizar orçamento
            updateBudgetDisplay(user.budget, totalSpent);
        }
        
        // Função para atualizar a exibição do perfil
        function updateProfileDisplay() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const user = usersData[userEmail];
            
            // Atualizar informações do perfil
            document.getElementById('profileName').textContent = user.name || userEmail.split('@')[0];
            document.getElementById('profileEmail').textContent = userEmail;
            
            // Formatar data de cadastro
            if (user.registrationDate) {
                const registrationDate = new Date(user.registrationDate);
                const options = { day: '2-digit', month: 'long', year: 'numeric' };
                const formattedDate = registrationDate.toLocaleDateString('pt-BR', options);
                document.getElementById('memberSince').textContent = formattedDate;
            } else {
                document.getElementById('memberSince').textContent = 'Data não disponível';
            }
            
            // Atualizar avatar
            const profileAvatar = document.getElementById('profileAvatar');
            const initials = user.name ? 
                user.name.split(' ').map(n => n[0]).join('').substring(0, 2).toUpperCase() : 
                userEmail[0].toUpperCase();
            profileAvatar.textContent = initials;
            profileAvatar.style.backgroundColor = getRandomColor(userEmail);
            
            // Atualizar informações pessoais
            document.getElementById('userName').value = user.name || '';
            document.getElementById('userPhone').value = user.phone || '';
            document.getElementById('userBirthday').value = user.birthday || '';
            
            // Atualizar configurações
            document.getElementById('userCurrency').value = user.currency || 'BRL';
            document.getElementById('userLanguage').value = user.language || 'pt-BR';
            document.getElementById('userTheme').value = user.theme || 'light';
            
            // Atualizar notificações
            document.getElementById('notifyExpenses').checked = user.notifications?.expenses !== false;
            document.getElementById('notifyReports').checked = user.notifications?.reports !== false;
            document.getElementById('notifyBudget').checked = user.notifications?.budget !== false;
        }
        
        // Gerar cor aleatória para o avatar baseada no email (para ser consistente)
        function getRandomColor(email) {
            const colors = ['#3498db', '#2ecc71', '#e74c3c', '#f39c12', '#9b59b6', '#1abc9c', '#d35400'];
            
            if (!email) return colors[0];
            
            // Gerar um hash simples do email para obter um índice consistente
            let hash = 0;
            for (let i = 0; i < email.length; i++) {
                hash = email.charCodeAt(i) + ((hash << 5) - hash);
            }
            
            const index = Math.abs(hash) % colors.length;
            return colors[index];
        }
        
        // Aplicar tema selecionado
        function applyTheme() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const theme = usersData[userEmail].theme;
            
            if (theme === 'dark') {
                document.documentElement.style.setProperty('--light-color', '#2c3e50');
                document.documentElement.style.setProperty('--dark-color', '#ecf0f1');
                document.body.style.backgroundColor = '#34495e';
                document.body.style.color = '#ecf0f1';
                
                // Ajustar cores dos containers
                const containers = document.querySelectorAll('.container, .card, .add-expense-form, .modal-content');
                containers.forEach(container => {
                    container.style.backgroundColor = '#2c3e50';
                    container.style.color = '#ecf0f1';
                });
                
                // Ajustar cores dos inputs
                const inputs = document.querySelectorAll('input, select');
                inputs.forEach(input => {
                    input.style.backgroundColor = '#34495e';
                    input.style.color = '#ecf0f1';
                    input.style.borderColor = '#7f8c8d';
                });
                
                // Ajustar cores das tabelas
                const tables = document.querySelectorAll('table');
                tables.forEach(table => {
                    table.style.color = '#ecf0f1';
                });
                
                const ths = document.querySelectorAll('th');
                ths.forEach(th => {
                    th.style.backgroundColor = '#3498db';
                });
                
                const trs = document.querySelectorAll('tr:nth-child(even)');
                trs.forEach(tr => {
                    tr.style.backgroundColor = '#34495e';
                });
            } else {
                // Reset para tema claro
                document.documentElement.style.setProperty('--light-color', '#ecf0f1');
                document.documentElement.style.setProperty('--dark-color', '#2c3e50');
                document.body.style.backgroundColor = '#f5f7fa';
                document.body.style.color = '#2c3e50';
                
                const containers = document.querySelectorAll('.container, .card, .add-expense-form, .modal-content');
                containers.forEach(container => {
                    container.style.backgroundColor = '';
                    container.style.color = '';
                });
                
                const inputs = document.querySelectorAll('input, select');
                inputs.forEach(input => {
                    input.style.backgroundColor = '';
                    input.style.color = '';
                    input.style.borderColor = '';
                });
                
                const tables = document.querySelectorAll('table');
                tables.forEach(table => {
                    table.style.color = '';
                });
                
                const ths = document.querySelectorAll('th');
                ths.forEach(th => {
                    th.style.backgroundColor = '';
                });
                
                const trs = document.querySelectorAll('tr:nth-child(even)');
                trs.forEach(tr => {
                    tr.style.backgroundColor = '';
                });
            }
        }
        
        // Função para atualizar totais no dashboard
        function updateTotals(fixedTotal, variableTotal) {
            document.getElementById('fixedExpenses').textContent = `R$ ${fixedTotal.toFixed(2).replace('.', ',')}`;
            document.getElementById('variableExpenses').textContent = `R$ ${variableTotal.toFixed(2).replace('.', ',')}`;
            document.getElementById('totalExpenses').textContent = `R$ ${(fixedTotal + variableTotal).toFixed(2).replace('.', ',')}`;
            
            // Atualizar também na seção de orçamento
            document.getElementById('spentAmount2').textContent = `R$ ${(fixedTotal + variableTotal).toFixed(2).replace('.', ',')}`;
        }
        
        // Função para atualizar a exibição do orçamento
        function updateBudgetDisplay(budget, spent) {
            const remaining = budget - spent;
            const remainingElement = document.getElementById('remainingAmount');
            const remainingElement2 = document.getElementById('remainingAmount2');
            
            document.getElementById('budgetAmount').textContent = `R$ ${budget.toFixed(2).replace('.', ',')}`;
            document.getElementById('spentAmount').textContent = `R$ ${spent.toFixed(2).replace('.', ',')}`;
            document.getElementById('remainingAmount').textContent = `R$ ${Math.abs(remaining).toFixed(2).replace('.', ',')}`;
            
            document.getElementById('budgetAmount2').textContent = `R$ ${budget.toFixed(2).replace('.', ',')}`;
            document.getElementById('remainingAmount2').textContent = `R$ ${Math.abs(remaining).toFixed(2).replace('.', ',')}`;
            
            // Alterar cor conforme o saldo
            if (remaining >= 0) {
                remainingElement.className = 'positive';
                remainingElement2.className = 'positive';
            } else {
                remainingElement.className = 'negative';
                remainingElement2.className = 'negative';
                remainingElement.textContent = `-R$ ${Math.abs(remaining).toFixed(2).replace('.', ',')}`;
                remainingElement2.textContent = `-R$ ${Math.abs(remaining).toFixed(2).replace('.', ',')}`;
            }
        }
        
        // Função para definir o orçamento mensal
        function setBudget() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            const budgetValue = parseFloat(monthlyBudgetInput.value) || parseFloat(monthlyBudgetInput2.value);
            if (isNaN(budgetValue)) return;
            
            // Atualizar dados do usuário
            usersData[userEmail].budget = budgetValue;
            saveUsersData(usersData);
            
            // Calcular total gasto
            const totalSpent = usersData[userEmail].expenses.reduce((sum, expense) => sum + parseFloat(expense.value), 0);
            
            // Atualizar exibição
            updateBudgetDisplay(budgetValue, totalSpent);
            monthlyBudgetInput.value = '';
            monthlyBudgetInput2.value = '';
        }
        
        // Função para adicionar nova despesa
        function addExpense() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            const date = document.getElementById('expenseDate').value;
            const description = document.getElementById('expenseDescription').value.trim();
            const value = document.getElementById('expenseValue').value;
            const category = document.getElementById('expenseCategory').value;
            const status = document.getElementById('expenseStatus').value;
            
            // Validar campos
            if (!date || !description || !value || !category || !status) {
                alert('Preencha todos os campos!');
                return;
            }
            
            if (parseFloat(value) <= 0) {
                alert('O valor da despesa deve ser maior que zero!');
                return;
            }
            
            // Adicionar despesa ao usuário
            usersData[userEmail].expenses.push({
                date,
                description,
                value: parseFloat(value),
                category,
                status
            });
            
            // Salvar dados atualizados
            saveUsersData(usersData);
            
            // Limpar formulário
            document.getElementById('expenseDescription').value = '';
            document.getElementById('expenseValue').value = '';
            document.getElementById('expenseDate').valueAsDate = new Date();
            
            // Recarregar dados
            loadUserData();
        }
        
        // Função para atualizar status de uma despesa
        function updateStatus(selectElement, index) {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            const newStatus = selectElement.value;
            usersData[userEmail].expenses[index].status = newStatus;
            
            // Salvar dados atualizados
            saveUsersData(usersData);
            
            // Atualizar classe da linha
            const row = selectElement.closest('tr');
            row.className = `status-${newStatus}`;
            
            // Recalcular totais
            recalculateTotals();
        }
        
        // Função para excluir despesa
        function deleteExpense(index) {
            if (!confirm('Tem certeza que deseja excluir esta despesa?')) return;
            
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            usersData[userEmail].expenses.splice(index, 1);
            
            // Salvar dados atualizados
            saveUsersData(usersData);
            
            loadUserData();
        }
        
        // Função para filtrar despesas
        function filterExpenses() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            const categoryFilter = document.getElementById('filterCategory').value;
            const statusFilter = document.getElementById('filterStatus').value;
            
            const filteredExpenses = usersData[userEmail].expenses.filter(expense => {
                const matchesCategory = !categoryFilter || expense.category === categoryFilter;
                const matchesStatus = !statusFilter || expense.status === statusFilter;
                return matchesCategory && matchesStatus;
            });
            
            // Limpar tabela
            expensesTableBody.innerHTML = '';
            
            // Preencher tabela com despesas filtradas
            filteredExpenses.forEach((expense, index) => {
                const row = document.createElement('tr');
                row.classList.add(`status-${expense.status}`);
                
                // Formatar data para exibição (dd/mm/aaaa)
                const dateObj = new Date(expense.date);
                const formattedDate = dateObj.toLocaleDateString('pt-BR');
                
                row.innerHTML = `
                    <td>${formattedDate}</td>
                    <td>
                        <select class="status-select" onchange="updateStatus(this, ${index})">
                            <option value="paid" ${expense.status === 'paid' ? 'selected' : ''}>Pago</option>
                            <option value="pending" ${expense.status === 'pending' ? 'selected' : ''}>Pendente</option>
                            <option value="overdue" ${expense.status === 'overdue' ? 'selected' : ''}>Atrasado</option>
                        </select>
                    </td>
                    <td>${expense.description}</td>
                    <td>R$ ${parseFloat(expense.value).toFixed(2).replace('.', ',')}</td>
                    <td>${expense.category}</td>
                    <td><button class="delete-btn" onclick="deleteExpense(${index})"><i class="fas fa-trash"></i> Excluir</button></td>
                `;
                
                expensesTableBody.appendChild(row);
            });
        }
        
        // Função para resetar filtros
        function resetFilters() {
            document.getElementById('filterCategory').value = '';
            document.getElementById('filterStatus').value = '';
            loadUserData();
        }
        
        // Função para recalcular totais
        function recalculateTotals() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail) return;
            
            const user = usersData[userEmail];
            const expenses = user.expenses;
            let fixedTotal = 0;
            let variableTotal = 0;
            let totalSpent = 0;
            
            expenses.forEach(expense => {
                const value = parseFloat(expense.value);
                totalSpent += value;
                
                if (expense.category === 'Despesas fixas') {
                    fixedTotal += value;
                } else {
                    variableTotal += value;
                }
            });
            
            updateTotals(fixedTotal, variableTotal);
            updateBudgetDisplay(user.budget, totalSpent);
        }
        
        // Função de logout
        function logout() {
            localStorage.removeItem('loggedInUser');
            loginContainer.style.display = 'block';
            appWrapper.style.display = 'none';
            document.getElementById('email').value = '';
            document.getElementById('password').value = '';
            errorMessage.style.display = 'none';
            closeModal();
        }
        
        // Funções para alteração de senha
        function openChangePasswordModal() {
            passwordModal.style.display = 'block';
        }
        
        function showRegisterModal() {
            registerModal.style.display = 'block';
        }
        
        function closeModal() {
            passwordModal.style.display = 'none';
            registerModal.style.display = 'none';
            deleteAccountModal.style.display = 'none';
            document.getElementById('currentPassword').value = '';
            document.getElementById('newPassword').value = '';
            document.getElementById('confirmPassword').value = '';
            document.getElementById('deletePassword').value = '';
            document.getElementById('registerName').value = '';
            document.getElementById('registerEmail').value = '';
            document.getElementById('registerPassword').value = '';
            document.getElementById('registerConfirmPassword').value = '';
        }
        
        function changePassword() {
            const currentPassword = document.getElementById('currentPassword').value;
            const newPassword = document.getElementById('newPassword').value;
            const confirmPassword = document.getElementById('confirmPassword').value;
            const currentUser = localStorage.getItem('loggedInUser');
            
            if (!currentUser || !usersData[currentUser]) return;
            
            // Verificar senha atual
            if (usersData[currentUser].password !== currentPassword) {
                alert('A senha atual está incorreta!');
                return;
            }
            
            if (newPassword !== confirmPassword) {
                alert('As senhas não coincidem!');
                return;
            }
            
            if (newPassword.length < 6) {
                alert('A senha deve ter pelo menos 6 caracteres!');
                return;
            }
            
            // Atualiza a senha no objeto de usuários
            usersData[currentUser].password = newPassword;
            saveUsersData(usersData);
            
            alert('Senha alterada com sucesso!');
            closeModal();
        }
        
        // Função para cadastrar novo usuário
        function registerUser() {
            const name = document.getElementById('registerName').value.trim();
            const email = document.getElementById('registerEmail').value.trim().toLowerCase();
            const password = document.getElementById('registerPassword').value;
            const confirmPassword = document.getElementById('registerConfirmPassword').value;
            
            // Validar campos
            if (!name || !email || !password || !confirmPassword) {
                alert('Preencha todos os campos!');
                return;
            }
            
            if (password !== confirmPassword) {
                alert('As senhas não coincidem!');
                return;
            }
            
            if (password.length < 6) {
                alert('A senha deve ter pelo menos 6 caracteres!');
                return;
            }
            
            if (!validateEmail(email)) {
                alert('Por favor, insira um e-mail válido!');
                return;
            }
            
            // Verificar se o e-mail já está cadastrado
            if (usersData[email]) {
                alert('Este e-mail já está cadastrado!');
                return;
            }
            
            // Criar novo usuário
            usersData[email] = {
                password: password,
                name: name,
                phone: '',
                birthday: '',
                registrationDate: new Date().toISOString(),
                expenses: [],
                budget: 0,
                currency: 'BRL',
                language: 'pt-BR',
                theme: 'light',
                notifications: {
                    expenses: true,
                    reports: true,
                    budget: true
                }
            };
            
            // Salvar dados
            saveUsersData(usersData);
            
            // Fazer login automaticamente
            localStorage.setItem('loggedInUser', email);
            loginContainer.style.display = 'none';
            appWrapper.style.display = 'flex';
            
            // Carregar dados do usuário
            loadUserData();
            updateProfileDisplay();
            
            alert('Cadastro realizado com sucesso!');
            closeModal();
        }
        
        // Função para validar e-mail
        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }
        
        // Funções para gerenciamento de perfil
        function saveProfile() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const name = document.getElementById('userName').value.trim();
            const phone = document.getElementById('userPhone').value.trim();
            const birthday = document.getElementById('userBirthday').value;
            const currency = document.getElementById('userCurrency').value;
            const language = document.getElementById('userLanguage').value;
            const theme = document.getElementById('userTheme').value;
            
            // Atualizar dados do usuário
            usersData[userEmail].name = name;
            usersData[userEmail].phone = phone;
            usersData[userEmail].birthday = birthday;
            usersData[userEmail].currency = currency;
            usersData[userEmail].language = language;
            usersData[userEmail].theme = theme;
            
            // Atualizar notificações
            usersData[userEmail].notifications = {
                expenses: document.getElementById('notifyExpenses').checked,
                reports: document.getElementById('notifyReports').checked,
                budget: document.getElementById('notifyBudget').checked
            };
            
            // Salvar dados
            saveUsersData(usersData);
            
            // Atualizar exibição
            updateProfileDisplay();
            
            // Aplicar novo tema se necessário
            applyTheme();
            
            alert('Perfil atualizado com sucesso!');
        }
        
        function confirmAccountDeletion() {
            deleteAccountModal.style.display = 'block';
        }
        
        function deleteAccount() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const password = document.getElementById('deletePassword').value;
            
            // Verificar senha
            if (usersData[userEmail].password !== password) {
                alert('Senha incorreta!');
                return;
            }
            
            // Confirmar exclusão
            if (!confirm('Tem certeza que deseja excluir sua conta permanentemente? Esta ação não pode ser desfeita.')) {
                return;
            }
            
            // Remover usuário
            delete usersData[userEmail];
            saveUsersData(usersData);
            
            // Fazer logout
            logout();
            
            alert('Sua conta foi excluída com sucesso.');
        }
        
        function exportUserData() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const userData = usersData[userEmail];
            const dataStr = JSON.stringify(userData, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = `financas_pessoais_${userEmail}_${new Date().toISOString().split('T')[0]}.json`;
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
        }
        
        // Funções para relatórios
        function generateReport() {
            const userEmail = localStorage.getItem('loggedInUser');
            if (!userEmail || !usersData[userEmail]) return;
            
            const reportType = document.getElementById('reportType').value;
            const month = parseInt(document.getElementById('reportMonth').value);
            const year = parseInt(document.getElementById('reportYear').value);
            
            // Filtrar despesas pelo mês e ano selecionados
            const filteredExpenses = usersData[userEmail].expenses.filter(expense => {
                const expenseDate = new Date(expense.date);
                return expenseDate.getMonth() + 1 === month && expenseDate.getFullYear() === year;
            });
            
            if (filteredExpenses.length === 0) {
                alert('Nenhuma despesa encontrada para o período selecionado!');
                return;
            }
            
            // Gerar relatório conforme o tipo selecionado
            if (reportType === 'monthly') {
                generateMonthlyReport(filteredExpenses);
            } else if (reportType === 'category') {
                generateCategoryReport(filteredExpenses);
            } else if (reportType === 'status') {
                generateStatusReport(filteredExpenses);
            }
            
            // Mostrar tabela com os dados
            document.getElementById('reportTableContainer').style.display = 'block';
        }
        
        function generateMonthlyReport(expenses) {
            // Ordenar por data
            expenses.sort((a, b) => new Date(a.date) - new Date(b.date));
            
            // Preencher tabela
            const tableBody = document.getElementById('reportTableBody');
            tableBody.innerHTML = '';
            
            expenses.forEach(expense => {
                const row = document.createElement('tr');
                const date = new Date(expense.date).toLocaleDateString('pt-BR');
                
                row.innerHTML = `
                    <td>${date} - ${expense.description}</td>
                    <td>R$ ${expense.value.toFixed(2).replace('.', ',')}</td>
                    <td>${expense.category}</td>
                    <td>${getStatusText(expense.status)}</td>
                `;
                tableBody.appendChild(row);
            });
            
            // Atualizar placeholder do gráfico
            const placeholder = document.querySelector('#reportChart .chart-placeholder');
            if (placeholder) {
                placeholder.innerHTML = `
                    <i class="fas fa-chart-line" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                    <p>Relatório Mensal</p>
                    <p style="font-size: 0.8rem;">Total de despesas: ${expenses.length}</p>
                    <p style="font-size: 0.8rem;">Valor total: R$ ${expenses.reduce((sum, e) => sum + parseFloat(e.value), 0).toFixed(2).replace('.', ',')}</p>
                `;
            }
        }
        
        function generateCategoryReport(expenses) {
            // Agrupar por categoria
            const categories = {};
            expenses.forEach(expense => {
                if (!categories[expense.category]) {
                    categories[expense.category] = 0;
                }
                categories[expense.category] += parseFloat(expense.value);
            });
            
            // Preencher tabela
            const tableBody = document.getElementById('reportTableBody');
            tableBody.innerHTML = '';
            
            for (const category in categories) {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${category}</td>
                    <td>R$ ${categories[category].toFixed(2).replace('.', ',')}</td>
                    <td></td>
                    <td></td>
                `;
                tableBody.appendChild(row);
            }
            
            // Atualizar placeholder do gráfico
            const placeholder = document.querySelector('#reportChart .chart-placeholder');
            if (placeholder) {
                placeholder.innerHTML = `
                    <i class="fas fa-chart-pie" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                    <p>Relatório por Categoria</p>
                    <p style="font-size: 0.8rem;">Total de categorias: ${Object.keys(categories).length}</p>
                `;
            }
        }
        
        function generateStatusReport(expenses) {
            // Agrupar por status
            const statuses = {
                paid: 0,
                pending: 0,
                overdue: 0
            };
            
            expenses.forEach(expense => {
                statuses[expense.status] += parseFloat(expense.value);
            });
            
            // Preencher tabela
            const tableBody = document.getElementById('reportTableBody');
            tableBody.innerHTML = '';
            
            for (const status in statuses) {
                if (statuses[status] > 0) {
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td>${getStatusText(status)}</td>
                        <td>R$ ${statuses[status].toFixed(2).replace('.', ',')}</td>
                        <td></td>
                        <td></td>
                    `;
                    tableBody.appendChild(row);
                }
            }
            
            // Atualizar placeholder do gráfico
            const placeholder = document.querySelector('#reportChart .chart-placeholder');
            if (placeholder) {
                placeholder.innerHTML = `
                    <i class="fas fa-chart-bar" style="font-size: 3rem; color: #ddd; margin-bottom: 10px;"></i>
                    <p>Relatório por Status</p>
                `;
            }
        }
        
        function getStatusText(status) {
            const statusTexts = {
                paid: 'Pago',
                pending: 'Pendente',
                overdue: 'Atrasado'
            };
            return statusTexts[status] || status;
        }
        
        function exportReport() {
            const table = document.getElementById('reportTable');
            if (!table) return;
            
            const rows = table.querySelectorAll('tr');
            if (rows.length <= 1) {
                alert('Gere um relatório antes de exportar!');
                return;
            }
            
            let csv = [];
            
            // Cabeçalho
            const headers = [];
            table.querySelectorAll('th').forEach(th => {
                headers.push(th.textContent);
            });
            csv.push(headers.join(','));
            
            // Dados
            table.querySelectorAll('tbody tr').forEach(tr => {
                const row = [];
                tr.querySelectorAll('td').forEach(td => {
                    row.push(td.textContent);
                });
                csv.push(row.join(','));
            });
            
            const csvContent = csv.join('\n');
            const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
            const url = URL.createObjectURL(blob);
            
            const link = document.createElement('a');
            link.setAttribute('href', url);
            link.setAttribute('download', `relatorio_financeiro_${new Date().toISOString().split('T')[0]}.csv`);
            link.style.visibility = 'hidden';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
        
        // Funções para navegação
        function showSection(sectionId) {
            // Esconder todas as seções
            document.querySelectorAll('.section').forEach(section => {
                section.style.display = 'none';
            });
            
            // Mostrar a seção selecionada
            document.getElementById(`${sectionId}Section`).style.display = 'block';
            
            // Atualizar título da página
            const titles = {
                'dashboard': 'Dashboard',
                'expenses': 'Despesas',
                'budget': 'Orçamento',
                'reports': 'Relatórios',
                'profile': 'Meu Perfil'
            };
            document.getElementById('pageTitle').textContent = titles[sectionId];
            
            // Atualizar menu ativo
            document.querySelectorAll('.menu-item').forEach(item => {
                item.classList.remove('active');
            });
            
            // Encontrar o item do menu correspondente e ativá-lo
            const menuItems = document.querySelectorAll('.menu-item');
            for (let item of menuItems) {
                if (item.getAttribute('onclick').includes(sectionId)) {
                    item.classList.add('active');
                    break;
                }
            }
            
            // Fechar sidebar em dispositivos móveis
            if (window.innerWidth <= 768) {
                sidebar.classList.remove('active');
            }
        }
        
        function toggleSidebar() {
            sidebar.classList.toggle('active');
        }
        
        // Permitir enviar formulário com Enter
        document.getElementById('expenseDescription').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                addExpense();
            }
        });
        
        document.getElementById('expenseValue').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                addExpense();
            }
        });
        
        monthlyBudgetInput.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                setBudget();
            }
        });
        
        monthlyBudgetInput2.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                setBudget();
            }
        });
        
        // Fechar modais ao clicar fora
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                closeModal();
            }
        };
    </script>
</body>
</html>
