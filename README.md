# BP_Enhancement
BP screen enhancement to add custom fields to the existing BP screen

BDT_ANALYZER
Using the above tarnsaction on the required screen enhancement on BP, we can find the corresponding section.
<img width="1274" height="431" alt="image" src="https://github.com/user-attachments/assets/600decdb-51c2-4d44-aa69-27bac3c977ac" />

first we need to create section for displaying our fields
<img width="1200" height="285" alt="image" src="https://github.com/user-attachments/assets/9fe4b756-ac5f-44c7-9da6-1b0c37c5c78b" />

then we need to assign our created section to corresponding screen
<img width="800" height="917" alt="image" src="https://github.com/user-attachments/assets/220b5387-50bd-44a4-8a75-fc486560e986" />
<img width="1058" height="463" alt="image" src="https://github.com/user-attachments/assets/98759bb4-5e36-4be1-b6b5-54b4fd8cfe66" />

now we have to create view
<img width="614" height="703" alt="image" src="https://github.com/user-attachments/assets/0a17d032-c905-4709-ad58-2a0f8d9ce9c5" />
<img width="832" height="256" alt="image" src="https://github.com/user-attachments/assets/fd7ab702-fa81-469b-953d-2bc603257de6" />
<img width="897" height="837" alt="image" src="https://github.com/user-attachments/assets/29a2ed7f-093f-49a2-8489-1eb545650079" />

here we need to create the function group, function module(with screen) and assign in the view



and then finally assign the view to section
<img width="656" height="336" alt="image" src="https://github.com/user-attachments/assets/21eb31d8-b237-46e2-990f-f1f1c7bae3bf" />
<img width="719" height="435" alt="image" src="https://github.com/user-attachments/assets/f567443e-2dfd-468b-9b1f-be6160c0af12" />
<img width="828" height="347" alt="image" src="https://github.com/user-attachments/assets/cdae4c86-f975-4725-9180-3074c8eb4f52" />

function module PBO
<img width="905" height="460" alt="image" src="https://github.com/user-attachments/assets/7bc5d706-fe95-487a-9582-cb60099d4e8e" />

  CALL FUNCTION 'PSSP_BUPA_GMSPONSOR_GET'
    IMPORTING
      e_gmsponsor = gmsponsor.
*     E_DATA            =
which will fill the existing entry in gmsponser strcutre

function module PAI
<img width="881" height="490" alt="image" src="https://github.com/user-attachments/assets/c10b3e8c-f087-4d8a-a94c-21c2b1025bf1" />

*Store Data from my screen into main SAP function group
  CALL FUNCTION 'PSSP_BUPA_GMSPONSOR_COLLECT'
    EXPORTING
      i_subname   = 'CI_GMSPONSOR'
      i_gmsponsor = gmsponsor.
here we have to specify the enhancement structure which holds custom fields and then the data will be saved against BP in corresponding GMSPONSER table







