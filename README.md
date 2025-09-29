# BuyTechTrendBot

## Purpose
A Telegram bot that facilitates cryptocurrency token promotion through trending fast-track services. The bot allows users to submit token addresses, validate them, collect group information, and process payments for promotional campaigns on the BuyTech platform.

## Flow
1. **Chain Selection** - User selects blockchain network for token
2. **Token Submission** - User provides token contract address
3. **Token Validation** - Bot validates Ethereum address format (0x + 40 hex characters)
4. **Group Selection** - User selects Telegram group with admin rights
5. **Group Link** - User provides Telegram group link for promotion
6. **Payment Options** - User selects promotion duration (8/16/32 hours with discounts)
7. **Payment Processing** - User sends ETH payment and transaction hash
8. **Confirmation** - Bot verifies payment and activates promotion

## Structure
```
BuyTechTrendBot/
├── main.py                          # Entry point and bot initialization
├── telegram_bot/
│   ├── app.py                       # Bot configuration and dispatcher setup
│   ├── handlers/
│   │   └── Call_Back.py             # Main command and callback handlers
│   ├── keyboards/
│   │   └── keyboard.py              # Inline keyboard layouts
│   ├── states/
│   │   └── all_states.py            # FSM state definitions
│   ├── Messages/
│   │   └── message.py               # Bot message templates
│   ├── Validations/
│   │   └── verifytoken_pattern.py   # Token address validation
│   ├── callback_factories/          # Callback data factories
│   └── supoortUtilis/
│       └── handler_sup.py           # Support utilities
└── .gitignore
```

## Language
**Python** - Asynchronous programming with modern async/await syntax

## Tools
- **aiogram** - Telegram Bot API framework
- **FSMContext** - Finite State Machine for conversation flow
- **CallbackQuery** - Inline keyboard interaction handling
- **StateFilter** - State-based message filtering
- **Regular Expressions** - Token address validation
- **InlineKeyboardMarkup** - Interactive bot interfaces
- **asyncio** - Asynchronous operation management
- **logging** - Bot activity monitoring
