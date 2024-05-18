// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract CustomToken {

    string public coinName = "CustomToken";
    string public coinAbbrv = "CTK";
    uint256 public totalAmount;

    mapping(address => uint256) public coinBalances;

    function create(address _to, uint256 _value) public {
        totalAmount += _value;
        coinBalances[_to] += _value;
    }

    function destroy(address _from, uint256 _value) public {
        require(coinBalances[_from] >= _value, "Insufficient balance to burn");
        totalAmount -= _value;
        coinBalances[_from] -= _value;
    }
}
