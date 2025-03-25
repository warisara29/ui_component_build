import { useState } from "react";

const UserList = () => {
  // Sample user data
  const usersData = [
    { id: 1, name: "John Doe", email: "john@example.com" },
    { id: 2, name: "Jane Smith", email: "jane@example.com" },
    { id: 3, name: "Alice Johnson", email: "alice@example.com" },
    { id: 4, name: "Bob Brown", email: "bob@example.com" },
  ];

  // State for search input
  const [search, setSearch] = useState("");

  // Filter users based on search query
  const filteredUsers = usersData.filter((user) =>
    user.name.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div className="max-w-md mx-auto p-4">
      {/* Search Bar */}
      <input
        type="text"
        placeholder="Search users..."
        className="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />

      {/* User List */}
      <div className="mt-4 space-y-3">
        {filteredUsers.length > 0 ? (
          filteredUsers.map((user) => (
            <div key={user.id} className="p-4 bg-white shadow-md rounded-md">
              <h2 className="text-lg font-semibold">{user.name}</h2>
              <p className="text-gray-500">{user.email}</p>
            </div>
          ))
        ) : (
          <p className="text-gray-500">No users found</p>
        )}
      </div>
    </div>
  );
};

export default UserList;
