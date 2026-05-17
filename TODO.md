# TODO


- [x] Add admin endpoint to approve/reject deposit transactions (POST /admin/deposits/{tx_id}/action)
- [x] Update deposit approval logic to set tx.status to completed/failed and credit user balance on approve


- [x] Update frontend/admin.html: add Approve/Reject buttons for deposit transactions in the All Transactions table, calling the new endpoint

- [x] Ensure pending -> completed updates reflected on refresh

- [x] Run quick lint/test: start backend and verify flow manually



