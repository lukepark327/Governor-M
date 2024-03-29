## `GovernorMikeDelegate`






### `initialize(address timelock_, address comp_, uint256 votingPeriod_, uint256 votingDelay_, uint256 proposalThreshold_)` (public)

Used to initialize the contract during delegator contructor




### `propose(struct GovernorMikeDelegateStorageV1.Issue[] issues_) → uint256` (public)

Function used to propose a new proposal with multiple issues.
Sender must have delegates above the proposal threshold




### `queue(uint256 proposalId)` (external)

Queues a proposal of state succeeded




### `queueOrRevertInternal(address target, uint256 value, string signature, bytes data, uint256 eta)` (internal)





### `execute(uint256 proposalId)` (external)

Executes a queued proposal if eta has passed




### `cancel(uint256 proposalId)` (external)

Cancels a proposal only if sender is the proposer, or proposer delegates dropped below proposal threshold




### `getIssue(uint256 proposalId, uint256 issueNum) → address[] targets, uint256[] values, string[] signatures, bytes[] calldatas, string description` (external)

Gets an issue of a proposal




### `getVotes(uint256 proposalId) → uint256[]` (external)

Gets actions of a proposal




### `getReceipt(uint256 proposalId, address voter) → struct GovernorMikeDelegateStorageV1.Receipt` (external)

Gets the receipt for a voter on a given proposal




### `state(uint256 proposalId) → enum GovernorMikeDelegateStorageV1.ProposalState` (public)

Gets the state of a proposal




### `_winnerIssue(uint256 proposalId) → uint256 winnerIssue` (internal)





### `_winnerIssueVotes(uint256 proposalId) → uint256 maxVotes` (internal)





### `castVote(uint256 proposalId, uint8 support)` (external)

Cast a vote for a proposal




### `castVoteWithReason(uint256 proposalId, uint8 support, string reason)` (external)

Cast a vote for a proposal with a reason




### `castVoteBySig(uint256 proposalId, uint8 support, uint8 v, bytes32 r, bytes32 s)` (external)

Cast a vote for a proposal by signature


External function that accepts EIP-712 signatures for voting on proposals.

### `castVoteInternal(address voter, uint256 proposalId, uint8 support) → uint96` (internal)

Internal function that caries out voting logic




### `isWhitelisted(address account) → bool` (public)

View function which returns if an account is whitelisted




### `_setVotingDelay(uint256 newVotingDelay)` (external)

Admin function for setting the voting delay




### `_setVotingPeriod(uint256 newVotingPeriod)` (external)

Admin function for setting the voting period




### `_setProposalThreshold(uint256 newProposalThreshold)` (external)

Admin function for setting the proposal threshold


newProposalThreshold must be greater than the hardcoded min


### `_setWhitelistAccountExpiration(address account, uint256 expiration)` (external)

Admin function for setting the whitelist expiration as a timestamp for an account. Whitelist status allows accounts to propose without meeting threshold




### `_setWhitelistGuardian(address account)` (external)

Admin function for setting the whitelistGuardian. WhitelistGuardian can cancel proposals from whitelisted addresses




### `_setPendingAdmin(address newPendingAdmin)` (external)

Begins transfer of admin rights. The newPendingAdmin must call `_acceptAdmin` to finalize the transfer.


Admin function to begin change of admin. The newPendingAdmin must call `_acceptAdmin` to finalize the transfer.


### `_acceptAdmin()` (external)

Accepts transfer of admin rights. msg.sender must be pendingAdmin


Admin function for pending admin to accept role and update admin

### `add256(uint256 a, uint256 b) → uint256` (internal)





### `sub256(uint256 a, uint256 b) → uint256` (internal)





### `getChainIdInternal() → uint256` (internal)






