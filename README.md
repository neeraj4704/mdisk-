# mdisk-
const fileInput = document.getElementById("file-input");
const fileTableBody = document.getElementById("file-table-body");

fileInput.addEventListener("change", function() {
  const file = fileInput.files[0];
  
  const fileRow = document.createElement("tr");
  const fileNameCell = document.createElement("td");
  const fileSizeCell = document.createElement("td");
  const downloadCell = document.createElement("td");
  
  fileNameCell.innerHTML = file.name;
  fileSizeCell.innerHTML = file.size;
  downloadCell.innerHTML = `<a href="${URL.createObjectURL(file)}" download>Download</a>`;
  
  fileRow.appendChild(fileNameCell);
  fileRow.appendChild(fileSizeCell);
  fileRow.appendChild(downloadCell);
  
  fileTableBody.appendChild(fileRow);
});
