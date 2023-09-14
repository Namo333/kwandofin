<script>
    import crystal1 from "../img/crystal1.svg";
    import crystal2 from "../img/crystal2.svg";
    import whitelogo from "../img/whitelogo.svg";
  import Wrapper from "./wrapper.svelte";

    let loanAmount = 0;
    let interestRate = 0;
    let loanTerm = 0;

    let totalAmount = 0;
    let monthlyPayment = 0;
    let overpayment = 0;

    function calculateLoan() {
        const interestRatePerMonth = interestRate / 100 / 12;
        const monthlyInterest = Math.pow(1 + interestRatePerMonth, loanTerm);
        monthlyPayment = loanAmount * (interestRatePerMonth * monthlyInterest) / (monthlyInterest - 1);
        totalAmount = monthlyPayment * loanTerm;
        overpayment = totalAmount - loanAmount;
    }
</script>

<div class="calc__block">
    <div class="calc__blockContent">
        <div class="calc__blockContentLeft">
            {#if totalAmount !== undefined && monthlyPayment !== undefined && overpayment !== undefined}
                <div class="calc__blockContentVozrat">
                    <h1 class="blockContent__title">Сумма возврата:</h1>
                    <p class="blockContent__text">{totalAmount.toLocaleString()} ₽</p>
                </div>
                <div class="calc__blockContentVozrat">
                    <h1 class="blockContent__title">Срок кредита в месяцах:</h1>
                    <p class="blockContent__text">{loanTerm}</p>
                </div>
                <div class="calc__blockContentVozrat">
                    <h1 class="blockContent__title">Ежемесячный платеж:</h1>
                    <p class="blockContent__text">{monthlyPayment.toLocaleString()} ₽</p>
                </div>
                <div class="calc__blockContentVozrat">
                    <h1 class="blockContent__title">Переплата:</h1>
                    <p class="blockContent__text">{overpayment.toLocaleString()} ₽</p>
                </div>
            {/if}

            <div class="calc__blockContentVvodContent">
                <label class="blockContentVvodContent__item">
                    <p class="blockContentVvodContent__itemText"><span>Сумма кредита, ₽:</span> <input class="blockContentVvodContent__itemTextInput" type="number" bind:value={loanAmount}  on:input={calculateLoan} /></p>
                    <input class="blockContentVvodContent__itemPolsunok" type="range" min="1" max="10000000" bind:value={loanAmount} on:input={calculateLoan} />
                </label>

                <label class="blockContentVvodContent__item">
                    <p class="blockContentVvodContent__itemText"><span>Годовая ставка, %:</span> <input class="blockContentVvodContent__itemTextInput" type="number" step="0.1" bind:value={interestRate} on:input={calculateLoan} /></p>
                    <input class="blockContentVvodContent__itemPolsunok" type="range" min="1" max="100" step="0.1" bind:value={interestRate} on:input={calculateLoan} />
                </label>
                
                <label class="blockContentVvodContent__item">
                    <p class="blockContentVvodContent__itemText"><span>Срок кредита, мес:</span> <input class="blockContentVvodContent__itemTextInput" type="number" bind:value={loanTerm} on:input={calculateLoan} /></p>
                    <input class="blockContentVvodContent__itemPolsunok" type="range" min="1" max="24" step="1" bind:value={loanTerm} on:input={calculateLoan} />
                </label>
            </div>
        </div>
    </div>
</div>

<style>
    
    .calc__block {
        position: relative;
        min-width: 400px;
        flex-shrink: 0;
        border-radius: 36px;
        backdrop-filter: blur(40px);
        padding: 23px 53px 50px 53px;
        background: rgba(255, 255, 255, 0.08);
        color: var(--color-text2);
    }

    .blockContent__title {
        font-family: Inter;
        font-size: 30px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        margin: 0;
        padding: 0;
    }

    .blockContent__text {
        font-family: Inter;
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        opacity: 0.6;
        margin: 0;
        padding: 0;
        padding-bottom: 10px;
    }

    .calc__blockContentVozrat:nth-child(n+2) {
        padding-top: 12px;
    }

    span {
        text-align: center;
        font-family: Inter;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        opacity: 0.4;
    }

    .blockContentVvodContent__itemPolsunok {
        width: 100%;
        height: 20px;
    }

    .calc__blockContentVvodContent {
        padding-top: 25px;
    }

    .blockContentVvodContent__itemTextInput{
        border-radius:10px;
        border: none;
        transition: .3s border-color;
        margin:10px 0;
        padding:10px;
        background-color: transparent;
        color: #fff;
        outline: none;
        -webkit-appearance: none;
        -ms-appearance: none;
        -moz-appearance: none;
        appearance: none;
    }

    /* Медиа-запросы */
    @media (max-width: 768px) {
        .calc__block {
            min-width: 300px;
            height: auto;
            padding: 15px;
        }

        .blockContent__title {
            font-size: 24px;
        }

        .blockContent__text {
            font-size: 20px;
        }

        .calc__blockContentVozrat:nth-child(n+2) {
            padding-top: 8px;
        }

        span {
            font-size: 14px;
        }

        .blockContentVvodContent__itemPolsunok {
            height: 10px;
        }

        .calc__blockContentVvodContent {
            padding-top: 15px;
        }
    }

</style>