let selectedAmount = 0;

function selectAmount(amount) {
  selectedAmount = amount;
  document.getElementById("customAmount").value = "";
  document.getElementById("message").textContent = `You selected $${amount}`;
}

function donate() {
  const custom = document.getElementById("customAmount").value;
  const amount = custom ? parseFloat(custom) : selectedAmount;

  if (!amount || amount <= 0) {
    document.getElementById("message").textContent = "Please enter or select a valid amount.";
    return;
  }

  document.getElementById("message").textContent = `Thank you for your generous donation of $${amount.toFixed(2)}!`;
}
