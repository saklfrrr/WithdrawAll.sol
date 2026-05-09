# WithdrawAll.sol
WithdrawAll.sol
pragma solidity ^0.8.20;
contract WithdrawAll {
    address public owner = msg.sender;

    function withdraw() public {
        require(msg.sender == owner);
        payable(owner).transfer(address(this).balance);
    }
}
