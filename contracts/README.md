# Smart Contracts - Смарт-контракты

## 📁 Структура проекта

```
contracts/
├── src/
│   ├── ModuleA/              # Identity Management
│   │   ├── Identity.sol
│   │   ├── ReputationToken.sol
│   │   └── interfaces/
│   ├── ModuleB/              # Work Distribution
│   │   ├── WorkRegistry.sol
│   │   ├── TASEngine.sol     # Task Assignment Score v3.0
│   │   └── DROVOracle.sol    # Distributed Reputation Oracle
│   ├── ModuleC/              # Governance
│   │   ├── Governance.sol
│   │   ├── VotingMachine.sol
│   │   └── EmergencyCouncil.sol
│   ├── ModuleD/              # Treasury
│   │   ├── Treasury.sol
│   │   ├── Distribution.sol
│   │   └── PaymentRouter.sol
│   └── ModuleE/              # W-Reserve
│       ├── WReserve.sol
│       ├── StabilizationFund.sol
│       └── ConstitutionalGuard.sol
├── interfaces/               # Интерфейсы взаимодействия
│   ├── IIdentity.sol
│   ├── IWork.sol
│   ├── IGovernance.sol
│   ├── ITreasury.sol
│   └── IWReserve.sol
├── libraries/                # Библиотеки и утилиты
│   ├── Math.sol
│   ├── SafeDistribution.sol
│   └── ReputationMath.sol
├── test/                     # Тесты
│   ├── Unit/
│   └── Integration/
└── scripts/                  # Скрипты деплоя
    ├── deployment/
    └── verification/
```

## 🎯 Основные контракты

### Модуль A: Identity
- **Identity.sol** - Основной контракт управления идентичностью
- **ReputationToken.sol** - Soulbound NFT для репутационного капитала (R-токен)

### Модуль B: Work  
- **WorkRegistry.sol** - Реестр задач и назначений
- **TASEngine.sol** - Алгоритм Task Assignment Score v3.0
- **DROVOracle.sol** - Децентрализованная оценка работы

### Модуль C: Governance
- **Governance.sol** - Основной контракт управления
- **VotingMachine.sol** - Механизм голосования W × √R
- **EmergencyCouncil.sol** - Функции экстренного управления

### Модуль D: Treasury
- **Treasury.sol** - Управление казначейством
- **Distribution.sol** - Алгоритм распределения W × √R
- **PaymentRouter.sol** - Маршрутизатор выплат

### Модуль E: W-Reserve
- **WReserve.sol** - Конституционный фонд стабилизации
- **StabilizationFund.sol** - Механизмы защиты гарантий
- **ConstitutionalGuard.sol** - Защита суверенного резерва

## 🛠 Установка и разработка

### Требования
- Node.js 18+
- Hardhat 2.19+
- Solidity 0.8.23+

### Установка
```bash
npm install
npx hardhat compile
```

### Тестирование
```bash
npx hardhat test
npx hardhat coverage
```

### Деплой
```bash
npx hardhat run scripts/deployment/deploy.ts --network <network>
```

## 🔐 Безопасность

### Аудиты
- [ ] Внутренний аудит кода
- [ ] Внешний security review  
- [ ] Формальная верификация

### Меры защиты
- Reentrancy protection
- Access control modifiers
- Input validation
- Emergency pause mechanisms

## 📊 Статус разработки

| Модуль | Статус | Готовность |
|--------|--------|------------|
| Module A | 🔄 В разработке | 40% |
| Module B | ⏳ Планирование | 10% |
| Module C | 🔄 В разработке | 30% |
| Module D | ⏳ Планирование | 15% |
| Module E | 📋 Проектирование | 5% |

## 🤝 Участие в разработке

### Code Style
- Solidity Style Guide соблюдение
- NatSpec комментарии для всех функций
- Comprehensive test coverage

### Процесс
1. Fork репозитория
2. Создайте feature branch
3. Напишите тесты для нового функционала
4. Откройте Pull Request

## 📄 Лицензия

Все смарт-контракты распространяются под лицензией **GPL-3.0-only**

```
// SPDX-License-Identifier: GPL-3.0-only
```

---

**Последнее обновление:** Октябрь 2025  
**Версия архитектуры:** 5.0  
**Сеть:** Ethereum Mainnet / Polygon / Arbitrum (TBD)
